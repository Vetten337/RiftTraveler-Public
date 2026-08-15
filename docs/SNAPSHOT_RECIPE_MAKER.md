# Rift Traveler Snapshot Recipe Maker

The Snapshot Recipe Maker is a developer and server-operator tool for creating
new Temporal Retort protocols from an arranged Retort. Instead of writing recipe
JSON by hand, an authorized developer stages the intended ingredients, liquid,
and outputs in-game and asks Rift Traveler to create a deterministic recipe
file.

The tool uses the same recipe model, validator, registry, matcher, execution
checker, and atomic batch executor as Rift Traveler's built-in protocols. It
does not create a second recipe format.

> **Developer tool:** All `/rtdev` commands require the Vintage Story
> `controlserver` privilege. Snapshot Mode clears the selected Retort after a
> separate confirmation command. Read the warning carefully and do not use a
> Retort containing anything you want to keep.

## What the Snapshot Maker can capture

A generated protocol can include:

- one to three solid item or block ingredients;
- exact collectible codes;
- explicitly authored wildcard codes;
- explicitly enabled mixed-variant aggregation;
- exact integer `temporalDust` requirements on a fired Crystal Growth Mold;
- one optional liquid requirement, including its exact liquid code and litres;
- one or two solid item or block outputs;
- a minimum operating temperature;
- a processing duration;
- a required clamped lid;
- progress that pauses when operating conditions are lost;
- automatically inferred mod requirements for staged foreign inputs, outputs,
  and liquids.

Snapshot V1 always creates recipes with these fixed properties:

```text
Enabled: true
Maximum temperature: none
Lid: clamped
Progress behavior: pause
Liquid consumption: true, when liquid is present
```

It does not currently author liquid outputs, output attributes, catalysts,
probability, durability-scaled results, multiple liquid tanks, or custom
failure effects.

## Retort staging layout

The Snapshot Maker reads these Retort slots:

```text
Slots 0-2: recipe ingredients
Slots 3-4: intended recipe outputs
Slot 5: internal liquid tank
```

At least one ingredient and one output are required. Snapshotting clones and
inspects the staged stacks; it does not consume, move, or replace them.

## Recommended workflow

### 1. Place and target a Temporal Retort

Stand close to the Retort and keep the crosshair on it while enabling Snapshot
Mode.

### 2. Review the clearing warning

```text
/rtdev retort snapshotmode on
```

This command does not clear anything. It explains that the selected Retort's
inputs, outputs, and liquid will be permanently removed if Snapshot Mode is
confirmed.

### 3. Confirm Snapshot Mode

Keep looking at the same Retort and run:

```text
/rtdev retort snapshotmode on confirm
```

Confirmation clears solid slots 0-4 and the liquid tank, then binds Snapshot
Mode to:

```text
Player UID + Retort position + dimension
```

While Snapshot Mode is active:

- the bound developer may manually edit output slots 3 and 4;
- other players and automation cannot insert into those output slots;
- Retort protocol processing is suspended;
- open-state Barrel processing is suspended;
- heat may still exist, but it cannot advance or complete a protocol.

### 4. Stage the ingredients

Place recipe ingredients in slots 0-2. By default, every staged stack is
captured using its exact collectible code and stack quantity.

For example:

```text
Slot 0: 1x rifttraveler:crystalgrowthmold-fired, temporalDust = 8
Slot 1: 8x game:clearquartz
```

### 5. Stage the outputs

Place the intended products in slots 3 and 4. These are examples of valid
solid outputs:

```text
Slot 3: 1x rifttraveler:temporalcrystal
Slot 4: 1x rifttraveler:crystalgrowthmold-fired
```

Output attributes are not supported in Snapshot V1. A fresh returned mold must
therefore have no `temporalDust` attribute.

### 6. Stage an optional liquid

Use normal Retort liquid-container interactions or the privileged fill command:

```text
/rtdev retort fill <liquidCode> <litres>
```

Example:

```text
/rtdev retort fill game:waterportion 10
```

If the Retort contains 10 litres of water when captured, the generated recipe
requires at least 10 litres of that exact liquid and consumes 10 litres on
successful completion.

If the Retort tank is empty, the generated recipe contains `liquid: null` and
requires an empty tank.

Useful liquid commands:

```text
/rtdev retort drain
/rtdev retort drain <litres>
/rtdev retort clear
```

`retort clear` clears the complete Retort, not only its liquid.

### 7. Create the snapshot

```text
/rtdev retort snapshot <protocolCode> <minimumTemperature> <durationSeconds> [inputOverrides]
```

Basic example using exact staged collectible codes:

```text
/rtdev retort snapshot prt-002 1100 90
```

Arguments:

- `protocolCode` is a new path-only identifier such as `prt-002`;
- `minimumTemperature` is the required temperature in degrees Celsius;
- `durationSeconds` is the required processing time in seconds;
- `inputOverrides` is optional and enables explicit wildcards or mixed variants.

A protocol code cannot contain a domain, whitespace, wildcards, or path
traversal. Use `prt-002`, not `rifttraveler:prt-002`.

## Wildcards and mixed variants

Snapshot recipes use exact input codes unless an override is supplied. The tool
never guesses that an ingredient should be a wildcard.

Override grammar:

```text
<slot>=<code>[,mixed]
```

Multiple overrides are separated with semicolons and passed as one quoted
argument:

```text
/rtdev retort snapshot prt-002 1250 100 "1=game:*quartz,mixed;2=game:*quartz,mixed"
```

Rules:

- only input slots 0, 1, and 2 may be overridden;
- the referenced slot must contain a stack;
- the wildcard must match the collectible staged in that slot;
- `mixed` enables different matching variants to contribute to one ingredient;
- item ingredients remain items and block ingredients remain blocks;
- identical overridden ingredients are grouped and their quantities are added;
- grouping follows the lowest contributing input-slot number.

Example: if slots 1 and 2 contain different quartz variants totalling eight,
overriding both as `game:*quartz,mixed` creates one eight-quartz ingredient.
During processing, the matcher may draw those eight pieces deterministically
from multiple matching stacks while leaving excess quartz untouched.

## Attribute capture

Snapshot V1 deliberately avoids copying every ItemStack attribute.

Currently supported recipe-relevant attribute:

```text
rifttraveler:crystalgrowthmold-fired
    temporalDust: exact integer
```

Known transient state such as temperature, freshness, transition state,
durability, and inventory bookkeeping is ignored. Other meaningful attributes
cause the snapshot to fail instead of being silently discarded. This prevents
the generated recipe from accepting an item whose important state was lost.

## Administrative slot staging

Output slots remain output-only during normal gameplay. Operators can stage
precise test stacks without Snapshot Mode by using:

```text
/rtdev retort setslot <0-4> <itemCode> <quantity>
/rtdev retort setslot <0-4> clear
```

Examples:

```text
/rtdev retort setslot 3 rifttraveler:temporalcrystal 1
/rtdev retort setslot 4 rifttraveler:crystalgrowthmold-fired 1
/rtdev retort setslot 3 clear
```

This command does not take items from the player's inventory. It is intended
for controlled development and server testing.

## Verification and file output

The Snapshot Maker does not report success immediately after serialization.
It performs this complete verification sequence:

```text
Build recipe model
    -> production validation
    -> deterministic JSON serialization
    -> atomic file write
    -> read the final file from disk
    -> deserialize it
    -> production validation again
    -> verify source and recipe identity
    -> semantic comparison with the staged recipe
```

If verification fails, the newly created file is removed. The staged Retort is
left unchanged and Snapshot Mode remains active so the developer can correct
the setup.

After verified success:

- the generated file remains on disk;
- staged ingredients, outputs, and liquid remain in the Retort;
- Snapshot Mode automatically turns off;
- normal output restrictions and processing resume;
- a server or world restart is required before the new recipe can load.

## Generated recipe location

Generated recipes are written under the active Vintage Story data directory:

```text
ModConfig/RiftTraveler/GeneratedTemporalRetortRecipes/<protocolCode>.json
```

Typical Windows location:

```text
%AppData%\VintagestoryData\ModConfig\RiftTraveler\GeneratedTemporalRetortRecipes\
```

Typical dedicated Linux server using `--dataPath ./data`:

```text
<server-root>/data/ModConfig/RiftTraveler/GeneratedTemporalRetortRecipes/
```

Only `.json` files directly inside this directory are scanned. Subdirectories
are not scanned, and live reload is not supported.

Packed mod recipes load before generated recipes. A generated recipe cannot
replace a packed recipe with the same identifier. Existing files are never
silently overwritten.

To remove a generated protocol, stop the server, remove its JSON file from this
directory, and restart. Back up the file first if it may be needed later.

## Experimentation, exploration, and discovery

The Snapshot Maker creates the mechanical protocol: what the Retort matches,
which conditions it requires, what it consumes, and what it produces.

The player Discovery system serves a different purpose. It controls:

- research-lead triggers;
- incomplete experimental clues;
- successful-completion confirmation;
- entries in the Temporal Discoveries Handbook.

During ordinary play, the Retort does not require players to select a recipe
from a menu. It evaluates the ingredients, liquid, lid, temperature, and output
space against registered protocols. This allows experimentation to remain part
of the gameplay: players arrange plausible materials and observe whether the
machine can sustain a reaction.

Built-in protocols such as PRT-001 have dedicated Discovery Catalog entries
that connect their gameplay triggers, clues, completion identity, and Handbook
presentation.

**A Snapshot-generated recipe automatically receives a generic research lead
and Handbook discovery entry after restart.** Possessing any of its solid
ingredients unlocks the lead. Successfully completing the process confirms the
protocol and reveals its full requirements.

Recipe packs may provide an authored Discovery Catalog definition for custom
lore or a specialized trigger. Authored definitions take priority over the
automatic entry.

This design supports two authoring layers:

```text
Snapshot Recipe Maker
    Creates and verifies the mechanical protocol

Discovery Catalog
    Adds automatic discovery coverage, with optional authored customization
```

## Sharing generated recipes

A generated JSON file can be copied to the same generated-recipe directory on
another server. That server must have:

- Rift Traveler installed on both server and clients;
- every mod that provides a referenced collectible;
- a compatible Rift Traveler recipe schema;
- no packed or generated recipe using the same identifier.

Restart the server after copying the file. Snapshot recipes record the domains
of staged foreign collectibles in `requiresMods`, so unavailable compatibility
recipes are skipped safely. Recipe authors distributing a formal content pack
should package recipes as mod assets and may provide custom localization and
Discovery Catalog content for a more tailored presentation.

## Troubleshooting

### No Retort is targeted

Stand within interaction range and aim directly at a placed Temporal Retort.

### Snapshot Mode refuses confirmation

Run `snapshotmode on` first, keep looking at the same Retort, and then run
`snapshotmode on confirm`.

### No inputs or outputs

Stage at least one occupied input in slots 0-2 and one occupied output in slots
3-4.

### Wildcard override does not match

The authored wildcard must match the actual staged collectible. Check the exact
collectible code with Retort diagnostics or creative inventory information.

### Unsupported attribute

The stack contains meaningful state that Snapshot V1 cannot express safely.
Use an unmodified output or author and validate the JSON extension manually.

### Duplicate protocol code

Choose a new code. Snapshot creation refuses a code already present in the
active registry or generated directory.

### Recipe does not appear after creation

Restart the server or world. Generated protocols are startup-loaded and do not
support live reload.

### Recipe loads but has no discovery page

Restart the server or world and acquire one of the recipe's solid ingredients.
Every enabled registered Retort recipe receives an automatic discovery entry.

## Quick command reference

```text
/rtdev retort snapshotmode on
/rtdev retort snapshotmode on confirm
/rtdev retort snapshotmode off

/rtdev retort setslot <0-4> <itemCode> <quantity>
/rtdev retort setslot <0-4> clear

/rtdev retort fill <liquidCode> <litres>
/rtdev retort drain [litres]
/rtdev retort clear

/rtdev retort snapshot <protocolCode> <minimumTemperature> <durationSeconds> [inputOverrides]

/rt recipe
/rtdev retort inspect
/rtdev help
```

Use `/rt recipe` while targeting a Retort to inspect matching and execution
status. Use `/rtdev retort inspect` for the complete server-authoritative machine
diagnostic.

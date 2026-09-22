System.Management.Automation.Runspaces.PipelineReader`1+<GetReadEnumerator>d__20[System.Object]
# Rift Traveler Snapshot Recipe Maker

The Snapshot Recipe Maker is an in game tool for server operators who have the
Vintage Story `controlserver` privilege. It creates, tests, installs, edits,
duplicates, reviews, and removes Temporal Retort recipes without requiring the
operator to write JSON or restart the server.

Open a Temporal Retort and select **Enable / Disable** under **Snapshot Recipe
Maker**. The first selection displays the clearing warning. Select it again to
confirm. Confirmation clears the Retort and enables editable output slots.
Recipe processing remains suspended until Snapshot Mode is disabled or a recipe
is successfully saved.

## GUI workflow

1. Drag one to three ingredients from the Creative inventory into **Inputs**.
2. Drag one or two result items into **Outputs**.
3. Add liquid with a container, then use **-1 L** and **+1 L** for exact amounts.
4. Enter a unique protocol code.
5. Set temperature and duration with the arrow buttons or text boxes.
6. Select the required lid position: open, closed, or clamped.
7. Use the default discovery hint or select **Hint: Custom** and write one.
8. Optionally configure **Input Variants**.
9. Select **Preview Recipe**, then **Test Staged Recipe**.
10. Select **Create and Validate Recipe**.

The test is server authoritative and does not consume staged contents. It checks
input allocation, liquid, output definitions, dependencies, duplicate protocol
codes, and overlaps with installed recipes. Temperature and lid are displayed
as runtime requirements because Snapshot Mode suspends processing and cannot
represent a live cooking test.

A verified recipe is written atomically, loaded into the active registry
immediately, and given an automatic Temporal Discovery entry. No server restart
is required.

## Input variants

Every occupied input starts as **Exact Item**. Select that button to use
**Selected Items**.

To build an accepted list:

1. Place a desired variant in that Retort input slot.
2. Select **Add Current Item**.
3. Swap another Creative item into the same slot.
4. Select **Add Current Item** again.
5. Repeat as needed.

The panel displays localized item names. **Clear List** removes the selection.
All selected alternatives must be items or all must be blocks.

**Mixed: Yes** allows different accepted alternatives to combine toward one
required quantity. For example, one Clear Quartz and one Rose Quartz can satisfy
a quantity of two. **Mixed: No** requires the quantity to come from a single
accepted collectible. Hover over the Mixed button for the same explanation.

Generated JSON stores visual selections as explicit `acceptedCodes`. Existing
wildcard recipes remain compatible and appear as **Advanced** when loaded for
editing.

## Preview and staged test

**Preview Recipe** performs immediate checks and summarizes the staged
ingredients, outputs, liquid, operating conditions, custom hint, and mod
requirements.

**Test Staged Recipe** asks the server to build the unsaved candidate with the
production builder and validator. Its report includes:

- whether the staged inputs match;
- how many items each input slot contributes;
- whether the liquid requirement is satisfied;
- runtime temperature and lid requirements;
- expected outputs;
- missing or invalid modded collectibles;
- duplicate protocol identifiers;
- overlapping installed recipes and registry ordering.

The test never advances processing or changes inventory.

## Installed recipe viewer

Select **Open Recipes** to browse every active Temporal Retort recipe. Packed mod
recipes are read only. Generated recipes provide these actions:

- **Edit** stages the recipe and preserves its protocol identity;
- **Duplicate** stages it as a copy and requires a new protocol code;
- **Remove Recipe** deletes it after confirmation.

Saving an edit replaces only its matching managed generated file. Successful
creation and replacement update the live registry immediately.

Removing a generated recipe also refreshes the registry and removes its
connected discovery records from saved and online player Handbooks. The recipe
and its discovery page disappear without a restart.

## Discoveries and item presentation

A generated recipe automatically receives an unconfirmed Temporal Discovery.
The default hint is based on a staged ingredient. A custom hint replaces that
generated observation text.

Confirmed discovery pages display localized collectible names and item pictures
for ingredients and outputs. Explicit selected alternatives are shown
individually. Creative only or otherwise unlinked collectibles retain their
name and picture without creating a broken Handbook link.

A player discovers the full recipe by completing it normally. Generated
discoveries are synchronized when recipes are created, replaced, or removed.

## Mod support

Installed mod items and blocks can be dragged directly into the staging slots
and selected as variants. The generated recipe records required foreign mod
domains. A server must have those referenced mods installed for the recipe to
load.

## Generated files and safety

Generated recipes are stored under the active Vintage Story data directory:

```text
ModConfig/RiftTraveler/GeneratedTemporalRetortRecipes/<protocolCode>.json
```

Creation uses deterministic serialization, an atomic write, readback,
production validation, source and identity checks, and a complete semantic
comparison. Failed verification rolls back the write and leaves Snapshot Mode
active for correction.

Generated recipes cannot replace packed mod recipes. Back up generated recipe
files before moving them between servers.

## Command compatibility

The GUI is the recommended workflow. Existing `/rtdev retort` commands remain
available for diagnostics, automation, and advanced wildcard authoring:

```text
/rtdev retort snapshotmode on
/rtdev retort snapshotmode on confirm
/rtdev retort snapshotmode off
/rtdev retort setslot <0-4> <itemCode> <quantity>
/rtdev retort fill <liquidCode> <litres>
/rtdev retort drain [litres]
/rtdev retort snapshot <protocolCode> <temperature> <seconds> [lid] [hint] [edit] [variants]
/rtdev retort inspect
```

Only users with `controlserver` can operate Snapshot Mode or change generated
recipes.

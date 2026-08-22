# Rift Traveler Player Guide

Rift Traveler is designed as a progression through observation,
experimentation, and infrastructure rather than immediate teleportation.

## Temporal Triangulator

The Temporal Triangulator detects, analyzes, and tracks temporal signals. Press
the normal tool-mode control (F by default) to cycle between Triangulation,
Anchor, Cargo, and Residue Extraction modes. Its indicator lights, moving
crystal display, and compass point change color with the selected mode.

Triangulation mode studies natural Rifts. Approach within ten blocks, aim the
scanner at the Rift, and hold use. Keep the energy connection on the target for
six seconds. Releasing use, moving out of range, or losing the target cancels
the current analysis. A completed analysis collapses the Rift, adds one lock,
and coats the scanner with two measures of Temporal Residue.

Analyze three different Rifts, then follow the directional HUD toward their
convergence. A blue Travel Rift forms roughly ten blocks away when the network
is stabilized. Hold use near it to synchronize and begin random long-distance
travel. The destination cannot be selected.

Nearby players may hold use at the Travel Rift to join the scanner owner's
group. The HUD and toast messages report who is joined. The owner holds use to
depart with the current group, up to eight travelers total. Only the owner
needs a Triangulator and the three recorded locks.

Anchor mode tracks the player's calibrated Travel Anchor and controls
Anchor-based travel.

Cargo mode tracks the player's Cargo Anchor, binds a Cargo Transmitter, and
controls shipment transmission.

While holding the Triangulator, press P to enter HUD positioning mode and drag
the scanner panel. Press P again to keep the new position. While positioning,
Shift+P resets the scanner to its default place below the minimap and coordinate
display, then exits positioning. The chosen position is remembered after the
client is closed. Hover the scanner with a visible cursor to review these controls.

## Temporal Residue

Each successfully analyzed natural Rift leaves two measures of Temporal Residue
on the Triangulator. Successful natural-Rift travel leaves four additional
measures. Controlled Anchor travel, cargo transmission, and failed travel add
none. The scanner stores up to twelve measures and reports the amount in its
tooltip.

Press F to select Residue Extraction mode, aim into open air, and use the
scanner. All stored Residue is recovered into inventory, or dropped nearby if
the inventory is full. Temporal smoke and a short pressure release confirm the
extraction.

## Temporal Anchors

A newly placed Anchor begins as a private, unassigned foundation and calibrates
for five seconds. Once ready, install one Temporal Crystal to specialize and
charge it as your Travel Anchor, or install one Cargo Transmitter to create
your Cargo Anchor. Each player may own one of each role, and either may be
constructed first.

Hold Sneak while placing another Anchor to remotely relocate an existing
unassigned foundation or Travel Anchor. Relocation does not consume another
Anchor item. A Travel Anchor also retains its installed Crystal and charge
while recalibrating at the new location.

Manually breaking a charged Travel Anchor returns its Temporal Crystal to your
inventory, or drops it at the Anchor when your inventory is full. Explosions
and unusual removal may still destroy the charge.

## Temporal Cargo

A Cargo Anchor is a private destination created by installing a Cargo
Transmitter into an eligible Anchor. Craft and place a second Cargo Transmitter
as the six-slot field endpoint. Bind it with the Triangulator in Cargo mode,
stage the cargo, then hold the scanner use control to transmit. Breaking an
empty Cargo Anchor returns its installed Transmitter. Legacy Cargo Storage
Boxes convert directly into Cargo Transmitters in the crafting grid.

Cargo Anchors cannot be relocated remotely because that could be used to move
their stored inventory without a cargo transmission. Resolve pending
deliveries, empty the Cargo Anchor, and break it manually before establishing
another one elsewhere.

Shipments are committed to persistent server escrow before the source is
cleared. A full or unloaded destination delays delivery instead of discarding
the cargo. Items with unsupported nested inventories, including filled
buckets, are intentionally rejected.

When Manifold is installed, Temporal Cargo may travel between dimensions. A
shipment to an unloaded dimension remains safely queued until that dimension
and its Cargo Anchor become available. Player travel between dimensions is not
currently supported.

## Temporal Retort

The Temporal Retort extends familiar Barrel chemistry with heat, clamping,
timed processing, liquids, and atomic multi-output reactions. Its vessel and
firebox begin as separate Fireclay forming projects that are fired, reinforced
with Fireclay Bricks, and assembled with the remaining machine components.

Place the Retort with its working face toward you. It occupies one real block
but its model forms a horizontal two-block workstation: the 50 L reaction
vessel and an adjacent open-front firebox. The firebox-side block must be empty
or already contain a Firepit, preventing the model from overlapping another
block.

Build, fuel, and light a normal vanilla Firepit by hand inside the open firebox.
The Retort may be placed before or after the Firepit. It remains idle until the
correctly positioned Firepit is burning. Active Temporal processing produces
smoke at the exhaust pipe. The fitted Retort shelters this attached Firepit from
rain; unrelated uncovered Firepits retain their normal weather behavior.

- Open: workstation and immediate Barrel-compatible interactions
- Closed: sealed Barrel-compatible processing
- Clamped: heated Temporal protocol processing

The animated lid opens into a hollow barrel-lined vessel and uses familiar
vanilla chest-like feedback. With the lid open, the vessel shows its stored
liquid. The surface height and appearance follow the quantity and liquid type
in the 50 L tank. The front heat gauge follows the Retort's live temperature.

A protocol never consumes its inputs unless every output can be inserted.
Progress may pause when temperature or lid requirements are lost and resume
when the conditions return.

When Rustbound Magic is installed, the optional Rust Condensation protocol
processes eight Rusty Dust in five litres of Temporal Solvent. Clamp the Retort,
maintain at least 400 C for 30 seconds, and the reaction produces two Temporal
Residue. This protocol is absent when Rustbound Magic is not installed.

## Discoveries

Important observations can create research leads without revealing a complete
recipe. Successfully completing an unknown process confirms it and records the
full protocol in the Temporal Discoveries section of the Survival Handbook.

New leads and confirmed protocols display a short on-screen notification with a
subtle sound in addition to the chat record. Existing discoveries do not replay
notifications when reconnecting.

The Discoveries overview links to a separate page for each visible lead or
confirmed protocol. Confirmed pages show ingredients, liquids, outputs, operating
temperature, duration, and lid requirements. Ingredient and output names link to
their normal Handbook entries; mixed families open a Handbook search.

Every enabled Retort recipe receives discovery coverage automatically.
Possessing one of a protocol's solid ingredients can reveal a generic research
lead when no specially authored lead exists.

Use:

```text
/rt discoveries
```

to review the server-authoritative discovery record.


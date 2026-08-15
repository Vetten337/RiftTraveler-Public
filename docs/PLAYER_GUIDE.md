# Rift Traveler Player Guide

Rift Traveler is designed as a progression through observation,
experimentation, and infrastructure rather than immediate teleportation.

## Temporal Triangulator

The Temporal Triangulator detects and tracks temporal signals. Its modes are
selected with Vintage Story's normal tool-mode control.

Triangulation mode studies natural rifts. Scan and record three suitable rift
signatures, follow the directional HUD toward their convergence, and stabilize
the resulting travel opportunity. Successful natural travel can move the
player thousands of blocks.

Anchor mode tracks the player's calibrated Travel Anchor and controls
Anchor-based travel.

Cargo mode tracks the player's Cargo Anchor, binds a Cargo Transmitter, and
controls shipment transmission.

## Temporal Residue

Successful natural-rift travel leaves Temporal Residue on the Triangulator.
The stored amount appears in its tooltip. Sneak and use the Triangulator while
aiming into open air to clean it and recover the accumulated material.

## Temporal Anchors

A newly placed Anchor begins as a private, unassigned foundation and calibrates
for five seconds. Once ready, install one Temporal Crystal to specialize and
charge it as your Travel Anchor, or install one Cargo Storage Box to create
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

A Cargo Anchor is a private destination created from an eligible Anchor. A
Cargo Transmitter holds up to six outgoing stacks. Bind it with the
Triangulator in Cargo mode, stage the cargo, then hold the scanner use control
to transmit.

Cargo Anchors cannot be relocated remotely because that could be used to move
their stored inventory without a cargo transmission. Resolve pending
deliveries, empty the Cargo Anchor, and break it manually before establishing
another one elsewhere.

Shipments are committed to persistent server escrow before the source is
cleared. A full or unloaded destination delays delivery instead of discarding
the cargo. Items with unsupported nested inventories, including filled
buckets, are intentionally rejected.

## Temporal Retort

The Temporal Retort extends familiar Barrel chemistry with heat, clamping,
timed processing, liquids, and atomic multi-output reactions.

Place the Retort with its working face toward you. It occupies one real block
but its model forms a horizontal two-block workstation: the 50 L reaction
vessel and an adjacent open-front firebox. The firebox-side block must be empty
or already contain a Firepit, preventing the model from overlapping another
block.

Build, fuel, and light a normal vanilla Firepit by hand inside the open firebox.
The Retort may be placed before or after the Firepit. It remains idle until the
correctly positioned Firepit is burning. Active Temporal processing produces
smoke at the exhaust pipe.

- Open: workstation and immediate Barrel-compatible interactions
- Closed: sealed Barrel-compatible processing
- Clamped: heated Temporal protocol processing

With the lid open, the vessel shows its stored liquid. The surface height and
appearance follow the quantity and liquid type in the 50 L tank.

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

Every enabled Retort recipe receives discovery coverage automatically.
Possessing one of a protocol's solid ingredients can reveal a generic research
lead when no specially authored lead exists.

Use:

```text
/rt discoveries
```

to review the server-authoritative discovery record.


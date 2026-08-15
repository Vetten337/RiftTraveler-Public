# Rift Traveler Changelog

## 0.3.1-alpha.2

- Redesigned the Temporal Retort as a horizontal workstation with a 50 L
  barrel-like reaction vessel and adjacent open-front firebox.
- The firebox uses a normal player-built, fueled, and lit vanilla Firepit; the
  Retort can be placed before or after it.
- Added player-facing placement in all four horizontal directions. Heat
  detection, liquid rendering, and exhaust smoke rotate with the model.
- Blocked placement when the firebox side would overlap an unrelated block.
- Restored the hollow open vessel and liquid surface whose height and texture
  reflect the stored amount and liquid type.
- Stabilized Retort textures across open, closed, and clamped lid states.
- Added cooking smoke from the exhaust during active Temporal processing.
- Added an isolated development profile, repeatable smoke/persistence testing
  guidance, and development-only persistence probe groundwork.
- Published a single forward-slash-path ZIP for Windows and Linux clients and
  servers running Vintage Story 1.22.6 Stable.

## 0.3.0

- Rebuilt and tested against Vintage Story 1.22.6 Stable.
- Newly placed Anchors now begin as unassigned foundations. After calibration,
  install a Temporal Crystal for a Travel Anchor or a Cargo Storage Box for a
  Cargo Anchor.
- Players may own one Travel Anchor and one Cargo Anchor, constructed in either
  order.
- Holding Sneak while placing another Anchor remotely relocates an existing
  unassigned foundation or Travel Anchor without consuming another Anchor item.
- Charged Travel Anchors retain their installed Crystal and charge during
  relocation.
- Manually breaking a charged Travel Anchor returns its Temporal Crystal to
  inventory or drops it nearby when inventory is full.
- Cargo Anchors must be emptied and broken manually before another is created;
  they cannot be remotely relocated or used to retrieve stored items.
- Separated Cargo Anchor records from unassigned-foundation reservations,
  fixing placement failures when the other Anchor role already exists.
- Updated Survival Handbook entries, item descriptions, and player guidance for
  the finalized Anchor rules.

## 0.3.0-dev.4

- Added the missing Temporal Retort crafting recipe.
- Added the Retort recipe to normal Survival Handbook crafting information.
- The recipe uses four supported bronze plates, three Fireclay Bricks, one
  Barrel, and one Temporal Gear.
- Retained the corrected cross-platform mod packaging for Linux and Windows.
- Published the Snapshot Recipe Maker developer guide.

## 0.3.0-dev.3

- First public alpha release for Vintage Story 1.22.3.
- Added natural-rift scanning, triangulation, and long-distance travel.
- Added personal Temporal Anchors and scanner-controlled Anchor travel.
- Added the private Cargo Anchor and Cargo Transmitter network.
- Added cross-dimensional cargo escrow and atomic delivery.
- Added the Temporal Retort and its data-driven recipe engine.
- Added Crystal Growth Molds, Temporal Crystals, Solvent, Dust, and Residue.
- Added renewable Temporal Residue from successful natural-rift journeys.
- Added research leads, confirmed discoveries, and Survival Handbook records.
- Added the developer-only Snapshot Recipe Maker.


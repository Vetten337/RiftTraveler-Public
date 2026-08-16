# Rift Traveler Changelog

## 0.4.0

- Targeted Vintage Story 1.22.7 Stable while retaining compatibility with
  1.22.6.
- Reworked natural-Rift scanning into an active six-second analysis. Hold use
  while aiming at a Rift from within ten blocks and keep the energy beam
  connected. A completed analysis collapses the Rift and records one lock.
- Added two measures of Temporal Residue for collapsing an analyzed Rift and
  four for successful natural-Rift travel, with a twelve-measure scanner limit.
- Added a dedicated Residue Extraction scanner mode with a matching icon,
  focused HUD, temporal smoke, and pressure-release feedback.
- Added group Travel Rifts for up to eight travelers, including nearby-player
  join guidance, participant toasts, roster feedback, and synchronized transit.
- Added staged departure and arrival effects for natural, controlled, and group
  teleportation.
- Added mode-colored indicator lights, moving crystal colors, a brighter tip
  crystal, compass-point glow, and an extendable proximity-driven antenna.
- Added scanner power, calibration, detection, and lock audio feedback.
- Added Anchor-to-Crystal energy arcs and corrected Anchor placement direction.
- Improved analyzed-Rift collapse reliability, including persisted and
  command-spawned Rifts after a server restart.
- Improved Cargo delivery notifications and queued-shipment feedback.
- Documented tested Manifold support for cross-dimensional Temporal Cargo.
- Updated in-game and public player guidance for all new interactions.

## 0.3.4

- Added explicit Vintage Story game and Survival 1.22.6 dependencies to release
  metadata, allowing the Mod Database to identify compatible game versions and
  ensuring required Survival systems load before Rift Traveler.
- Includes all gameplay, discovery, Retort, and HUD improvements from 0.3.3.

## 0.3.3

- Added a persistent, movable Temporal Triangulator HUD. Press P while holding
  the scanner to position it; press Shift+P while positioning to reset and exit.
- Kept the minimap and coordinate readout in their native map-aligned positions
  when moving or resetting the scanner HUD.
- Added hover guidance for scanner positioning controls.
- Added queued on-screen notifications and a subtle sound for new research leads
  and confirmed protocols without replaying them during login synchronization.
- Split Temporal Discoveries into an overview and separate uncluttered pages.
- Added a complete confirmed-protocol recipe viewer with inputs, liquids, outputs,
  temperatures, duration, lid state, and processing behavior.
- Added direct Handbook links for exact recipe collectibles and search links for
  wildcard or mixed-variant ingredients.
- Added the distinct Temporal Gear Extraction lead after obtaining Temporal
  Solvent and prevented duplicate generic lead text.
- Protected the Retort's correctly oriented vanilla Firepit from rain while
  preserving vanilla weather behavior for ordinary uncovered Firepits.
- Grouped Retort directional variants into one Handbook identity, removing
  repeated Retort icons from compatible-container listings.
- Published one platform-neutral ZIP for Windows and Linux clients and servers
  running Vintage Story 1.22.6 Stable.

## 0.3.2

- Added optional compatibility with Rustbound Magic 3.2.5.
- Added Rust Condensation: eight Rusty Dust, five litres of consumed Temporal
  Solvent, at least 400 C, 30 seconds, and a clamped Retort produce two Temporal
  Residue.
- Added optional `requiresMods` declarations to Retort recipes. Recipes with an
  unavailable dependency are skipped safely.
- Snapshot Recipe Maker now infers required mods from staged foreign inputs,
  outputs, and liquids and preserves them through verification.
- Every enabled Retort recipe now gains automatic Temporal Discovery coverage
  when it has no authored discovery definition.
- Possessing a recipe ingredient unlocks the generated research lead; successful
  processing confirms and reveals the complete protocol.
- Authored discovery definitions retain priority for custom lore and triggers.
- Published one platform-neutral ZIP for Windows and Linux clients and servers
  running Vintage Story 1.22.6 Stable.

## 0.3.1

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


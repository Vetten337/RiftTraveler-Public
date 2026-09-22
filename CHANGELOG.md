# Rift Traveler Changelog

## 0.6.9

- Added the in game Snapshot Recipe Maker GUI for privileged server operators, including native staging, liquid controls, temperature, duration, lid selection, and default or custom discovery hints.
- Added live creation, validation, editing, duplication, browsing, and removal of generated Retort recipes without a server restart.
- Added visual exact and selected input alternatives, mixed quantity support, installed mod item support, and backward compatibility for wildcard recipes.
- Added recipe preview and server authoritative staged testing with input allocation, liquid, dependencies, outputs, duplicate code, and overlap reporting.
- Generated recipes now receive live automatic discoveries with localized names and item pictures. Removing a recipe also removes its connected Handbook discovery records.
- Added matching animated Rift presentation inside loaded Rift Harvesters.

## 0.6.8

- Reworked Rift Resonance Array deployment and its central Conflux reveal.
- Added animated Rift presentation to Array chargers, sconces, and placed Rift Cores.
- Expanded ground, shelf, and rack presentation for temporal materials and fixed Cargo Transmitter escrow pickup behavior.
- Improved Temporal Storm Stabilizer transitions and added its survival recipe.
## 0.6.7

- Added the Temporal Storm Stabilizer: place a compact Conflux box that extends its base and reconstructs into a complete machine with articulated arms, segmented gyroscopic rings, conduits, and four Crystal pedestals.
- Install a removable Stabilized Rift Core for automatic storm startup and shutdown. Optional Crystals extend the full-strength radius from 16 blocks with none, to 32 with four empty Crystals, and 64 with four full Crystals. Mixed charge levels produce intermediate ranges.
- The animated spherical shield uses the same radius as protection. During temporal storms it suspends personal instability and prevents new hostile spawns inside. Existing enemies can still enter; it is not a physical or general damage barrier.
- Added a central energy beam, branching shield energy, particles, and smooth storm ambience and stability-gear transitions when crossing the boundary.
- Added mechanical and temporal unpacking, deployment, ring connection, and reverse shutdown sounds synchronized with machine motion.
- Improved staged placement and cached animation preparation to reduce placement/loading stalls, and simplified machine selection outlines.
- Added the detailed Stabilizer handbook guide, item tooltip, packed item model, and user-tuned hand/ground transforms.
- The Stabilizer is currently available through Creative/admin placement; a survival crafting recipe is not included. Installed core and Crystal charge are not consumed by it.

- Rift locks now persist per player across logout, reconnect, server reload, and chunk unloading. Lock order, convergence center, stabilization, and pending resolution are preserved. Use `/rt reset` to abandon a cycle.
- In Rift mode, aim at a stabilized blue convergence within ten blocks and hold use for approximately six seconds to collapse it without a Harvester. Collapse stores up to four Temporal Residue, clears the three locks, and resumes Rift searching. Extract stored Residue first to make room.
- A prepared Rift Harvester within ten blocks takes priority and captures a Stabilized Rift Core instead. Travel mode remains the way to use the blue Rift for travel.
- Blue convergence collapse now shares the natural Rift's scanner tether, energy particles, glow, waveform, progress display, and audio. Releasing use, changing modes, leaving range, or looking away interrupts collapse without a reward or consuming the Rift.
- Saved lock and resolution records prevent repeated rewards after reconnecting or reloading.
- Fixed discovery notification text overlap for wrapped research titles, including Conflux Binding Compound and Temporal Gear Extraction.
- Chiseling a Conflux Iron ingot now produces twenty Conflux Iron Nuggets. Existing Conflux Iron metal bits convert one for one into nuggets in the crafting grid, restoring access to Conflux Binding Compound research.
- Updated the player handbook with saved tracking, convergence collapse, Harvester priority, Residue capacity, and metal-bit conversion instructions.

Install on both client and server. Existing players without saved tracking data start with an empty cycle; locks lost before this update cannot be recovered.

## 0.6.5

- Added the six-station Rift Resonance Array with clockwise alignment, a separate charging rotor, sliding chamber windows, charging particles, frame arcs, and clearer charged crystal models.
- Temporal Crystals now retain usable charge through storage, machine insertion, placement, pickup, saving, and Anchor relocation. Legacy charged crystals upgrade when used.
- Temporal Drives consume crystal energy and stop at depletion without destroying the crystal. Default full capacity is 30 minutes.
- Charged crystals support six Anchor returns or paired Gate departures at default settings. Departing Gates pay the charge cost; failed travel refunds it. Uncharged Anchor crystals remain single-use by default. Sneak-use an Anchor with an empty hand to retrieve its reusable crystal.
- Added server settings for crystal capacity, Anchor and Gate jump costs, uncharged Anchor crystal consumption, and Rift Core maximum charge.
- The Array accepts partially charged crystals. Rift Cores retain their unused percentage and become empty Containment Cores only when depleted.
- Array transfer time scales with energy supplied: a full refill takes at most 60 seconds, even with custom crystal capacity. Alignment and cooldown remain separate. Cycle timing and energy survive saving and reloading.
- Each crystal reaching full charge deposits four Temporal Residue in the Array's base tray. Incomplete transfers do not award completion residue.
- Reduced Conflux Iron infusion to 1 L of solvent per Iron Bloom, preserving one Temporal Bloom output. Temporal Quartz infusion uses 4 L per batch. Rust condensation uses 8 Rusty Dust and 1 L of solvent to produce 4 Temporal Residue.
- Refined Array textures and geometry, corrected overlapping surfaces, and improved machine animation lifecycle handling.
- Updated player handbook entries and tutorials for crystal consumption, recharging, core percentages, residue collection, and proportional charging time.

## Updating

Replace the previous Rift Traveler package with this ZIP on both client and server. Existing server settings are retained; new settings receive defaults. Already-used crystals retain their remaining energy when capacity changes—top them up in the Array to reach the new maximum.

Dependencies remain Vintage Story and Survival 1.22.6 or later within the supported 1.22.6–1.22.7 release line. This update does not raise the declared game requirement.

## 0.6.4

- Restored barrel-style proportional batching for Temporal Retort recipes.
- Temporal Solvent can now be produced in batches up to the Retort's full
  50-litre capacity while preserving the one Dust per litre recipe ratio.
- Scaled Retort batches now account for available ingredients, liquid volume,
  liquid conversion compatibility, and solid-output capacity before committing.
- Preserved atomic processing: invalid ratios or insufficient output space do
  not partially consume recipe contents.

## 0.6.3

- Added optional Immersive Woodworking 1.2.0 compatibility for Conflux Iron
  Sawmill Blades with iron-equivalent durability.
- Added Conflux Iron nails and strips to the supported vanilla metal variants.
- Completed current-game Conflux Iron metal-sheet, plain-sheet, and tarnished
  texture variants and removed the associated startup warnings.
- Removed unresolved `sawmillblade-confluxiron` recipe errors when both mods are
  loaded together.

## 0.6.2

- Added the Temporal Drive, a crystal-powered mechanical source that contributes
  torque, freewheels above its target speed, and supports combined networks.
- Added animated internal machinery, glass shielding, temporal arcs, particles,
  sound, directional effects, and save/reload recovery for the Temporal Drive.
- Expanded Temporal Retort research with structured discovery hints, progression
  guidance, and new Conflux Binding Compound, Temporal Quartz, Containment
  Insulator, and Temporal Solvent protocols.
- Moved Temporal Solvent production into the Retort and removed obsolete legacy
  Cargo Storage Boxes and their Handbook guidance.
- Added Survival Handbook guides and four native tutorials covering first scans,
  Rift capture, Travel Anchor returns, and Temporal Cargo transportation.
- Added explicit tutorial equipment checklists, restart-safe preflight pages,
  and a dedicated N confirmation key.
- Refined recipes, Handbook links, grouped Retort entries, discovery notices,
  directional visuals, mechanical persistence, and multiple block models.
- Published one platform-neutral ZIP for Windows and Linux clients and servers
  running supported Vintage Story 1.22.6-1.22.7 builds.

## 0.6.0

- Added the complete Conflux Iron production chain through Temporal Solvent,
  Retort-infused Temporal Blooms, anvil consolidation, nuggets, Bloomery
  recycling, and the standard iron component and tool family.
- Added reusable Containment Cores and a Rift Harvester for capturing natural
  Temporal Rifts and stabilized blue Convergence Rifts.
- Added Rift Core Sconces. Stabilized Rift Cores provide passive 50-block
  natural-rift warding when installed.
- Added functional five-by-five Convergence Gates built from Conflux Frame
  Blocks, Rift Containment Braces, and a player-facing Core Housing.
- Added authentic contained blue Convergence Rift visuals, staged activation,
  controlled collapse, Anchor-style audio, animated circuit pulses, and
  cyan/red operational indicators.
- Added gate names, paired destination selection, ownership, public/private
  access, allowed-player lists, safe bidirectional arrivals, and obstruction
  protection.
- Added a controlled-travel cancellation watchdog to recover from interrupted
  Anchor transitions without leaving the client behind a blue overlay.
- Improved Temporal Triangulator presentation and updated Survival Handbook
  guidance throughout.
- Published one platform-neutral ZIP for Windows and Linux clients and servers
  running supported Vintage Story 1.22.6-1.22.7 builds.

## 0.5.0

- Rebuilt the Temporal Retort as a cohesive oven-scale ceramic workstation
  while preserving its vessel-left, firebox-right function.
- Added separate Fireclay forming, firing, Fireclay Brick reinforcement, and
  assembly stages for the Retort vessel and firebox.
- Added a roofed firebox, open chimney and transfer pipe, bronze clamps, working
  heat gauge, barrel-lined hollow vessel, animated lid, and improved audio.
- Preserved vanilla Firepit fueling and ignition and made Retort removal clean
  up its attached Firepit while returning remaining fuel.
- Unified Temporal Cargo around one Cargo Transmitter item used for both the
  installed Cargo Anchor receiver and the separate field endpoint.
- Redesigned the Cargo Transmitter as a hollow vanilla-style chest with bronze
  temporal fittings, lid animation, vanilla chest sounds, and improved GUI.
- Added three-stage Anchor arm animations and matching particles, arcs, and
  activation sounds for both Crystals and mounted Cargo Transmitters.
- Improved Triangulator item displays and softened teleport edge particles.
- Published one platform-neutral ZIP for Windows and Linux clients and servers
  running supported Vintage Story 1.22.6-1.22.7 builds.

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


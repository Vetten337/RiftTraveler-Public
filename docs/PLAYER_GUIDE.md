# Rift Traveler Player Guide

Rift Traveler is designed as a progression through observation,
experimentation, and infrastructure rather than immediate teleportation.

Current release: **0.6.6**.

- [Temporal Storm Stabilizer](#temporal-storm-stabilizer)
- [Rift Resonance Array](#rift-resonance-array)
- [Temporal Crystal Charge](#temporal-crystal-charge)
- [Temporal Drive](#temporal-drive)

## Temporal Triangulator

**Temporal Triangulation and Rift Travel**

The Temporal Triangulator separates rift research from portal activation so collection cannot accidentally trigger long-distance travel.

**Rift Mode: Scan and Harvest**
Hold right-click while aiming at a natural Rift from within ten blocks. Keep the beam connected for six seconds. A successful analysis collapses the Rift, deposits two measures of Residue, and records one of three triangulation locks. A Rift Harvester loaded with an empty Containment Core and placed within ten blocks captures the rift as a Rift Core. After three locks, follow the display to the convergence and stabilize the blue Convergence Rift.

A stabilized blue Convergence Rift remains safe in Rift mode. With a prepared Harvester within ten blocks, aim at it and hold right-click to create a Stabilized Rift Core. Harvester capture takes priority.

**Collapse a Blue Rift for Residue**
Without a prepared Harvester, use Rift mode to aim at the stabilized blue Convergence Rift from within ten blocks and hold right-click continuously for approximately six seconds. The scanner beam, moving energy, waveform, progress display, and sounds indicate the collapse. Completion closes the blue Rift and stores up to four Temporal Residue in the Triangulator. It produces no Stabilized Rift Core. The three locks clear and normal Rift searching resumes.

Releasing use, looking away, leaving range, or changing modes interrupts collapse without consuming the convergence or awarding Residue. Aim again and begin a new hold to retry. A prepared Harvester appearing nearby interrupts collapse so you can capture the Rift instead.

**Travel Mode: Activate**
Select Travel mode, approach the stabilized blue Convergence Rift, aim at it, and hold right-click to synchronize and begin random long-distance travel. Nearby players may hold use to join before departure. Travel mode never harvests or scans rifts. Random travel cannot target a chosen destination. Successful passage drains personal temporal stability and deposits four additional measures of Residue on the owner's Triangulator.

**Saved Tracking Progress**
Your ordered Rift locks and calculated convergence center survive logout, reconnect, server reload, and chunk unloading. Changing modes does not abandon the cycle. With fewer than three locks, continue searching for the next distinct natural Rift. The same Rift ID and Rifts within eight blocks of an existing lock cannot be locked again in that cycle. With three locks, follow the saved center guidance. An unresolved blue Rift remains available for capture, collapse, or travel after reconnecting; interrupted use actions require a fresh hold.

Capture, collapse, or successful travel completes the cycle and clears its three locks. Use **/rt reset** to deliberately abandon your current tracking cycle and remove its convergence.

**Residue Extraction Mode**
The instrument stores up to twelve measures. Extract stored Residue before collapsing a blue Rift if you want room for the full four-measure reward; any amount beyond the available capacity is not stored. Aim into open air and use this mode to recover all stored Residue.

**Anchor Mode**
Tracks and activates a calibrated Travel Anchor for controlled return travel. An uncharged Crystal provides one disposable return; a charged Crystal provides up to six returns and can be recharged. Read Temporal Anchor for removal and charging instructions.

**Cargo Mode**
Tracks Cargo Anchors, binds Cargo Transmitters, and transmits staged cargo.

**Constructed Gates**
A harvested Stabilized Rift Core can power a constructed Convergence Gate. Constructed gates use their own Core Housing interface and do not require a Triangulator to enter.

**Safety Rule**
Rift mode means scan, harvest, or deliberately collapse a blue convergence. Travel mode means enter a stabilized blue Convergence Rift. Switching modes does not remove the ready portal.

*The origin of the temporal network remains unknown. Whether these pathways were created intentionally or are scars left upon reality remains a matter of debate.*

## Temporal Residue

Each successfully analyzed natural Rift leaves two measures of Temporal Residue
on the Triangulator. Successful natural-Rift travel leaves four additional
measures. Controlled Anchor travel, constructed Convergence Gate travel, cargo
transmission, and failed travel add none. The scanner stores up to twelve measures and reports the amount in its
tooltip.

Press F to select Residue Extraction mode, aim into open air, and use the
scanner. All stored Residue is recovered into inventory, or dropped nearby if
the inventory is full. Temporal smoke and a short pressure release confirm the
extraction.

## Temporal Anchors

**Temporal Anchor**

An Anchor begins as a private, unassigned foundation. Placement starts a five-second calibration and binds the foundation to its owner.

**Choosing a Role**
After calibration, install one Temporal Crystal to specialize the foundation as a charged Travel Anchor, or install one Cargo Transmitter to create an 18-slot Cargo Anchor. Each player may own one Travel Anchor and one Cargo Anchor, and either role may be established first.

**Travel Anchor**
The Temporal Triangulator's Anchor mode detects your Travel Anchor and reports its direction, distance, charge, and travel readiness. When Travel reports Ready, hold use and remain still through synchronization. Successful controlled travel returns you beside the Anchor. An uncharged Crystal is consumed for one return; a charged Crystal spends one sixth of its full capacity per return and remains reusable.

**Relocating Foundations and Travel Anchors**
Hold Sneak while placing another Anchor to relocate your existing unassigned foundation or Travel Anchor remotely. This is a relocation: the Anchor item is not consumed. A Travel Anchor retains its installed Crystal and charge while recalibrating at the new location.

**Breaking a Travel Anchor**
Breaking a Travel Anchor manually returns its installed Crystal, including a depleted reusable Crystal, to the breaker. It enters inventory when space is available or drops at the Anchor. Explosions and unusual removal can still destroy the charge.

**Cargo Anchor Restriction**
Cargo Anchors cannot be relocated remotely. Visit the Cargo Anchor, resolve pending deliveries, empty it, and break it manually before creating another. Breaking it returns the installed Cargo Transmitter.

*The temporal network recognizes one destination of each specialized role per traveler.*

**Crystal Charge**
A fully charged Crystal holds 30 minutes of energy by default. Item and machine information shows remaining time and available jumps. Server settings can change the full duration. Anchor and paired Gate travel each require one sixth of a full charge: five minutes by default, allowing six jumps from a full Crystal. Charge also spent in a Temporal Drive reduces the jumps available. A partially charged Crystal with less than one jump remaining must be topped up before travel.

**Disposable and Reusable Crystals**
An uncharged Crystal powers one Anchor return and is consumed by that jump. A charged Crystal instead spends one sixth of its full capacity per return and remains reusable after depletion. Failed travel refunds reserved charge. Sneak-use the Anchor with an empty hand to remove its reusable Crystal, then recharge it in the Rift Resonance Array. Remove the installed reusable Crystal before inserting another or converting the Anchor to cargo. A partially charged Crystal needs enough energy for a whole jump to be installed.

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

## Conflux Iron

Mix one Temporal Dust with one litre of Limewater in a Barrel to create one
litre of Temporal Solvent. A discoverable high-temperature, clamped Retort
protocol infuses an Iron Bloom with Solvent and produces a Temporal Bloom. Heat
the Bloom above 700 C and work it on an iron-tier anvil to consolidate one
Conflux Iron ingot.

Conflux Iron supports the standard iron components, tools, and weapons with
iron-equivalent performance. Chiseling one ingot produces twenty nuggets;
twenty nuggets consolidate back into one ingot in a Bloomery. Plates, rods,
and nuggets form the principal Convergence Gate components.

## Rift Capture and Sconces

Install one empty Containment Core in a Rift Harvester and place it within ten
blocks of a target. Complete a scan with the Triangulator in Rift mode. A
natural Temporal Rift becomes a Rift Core; a stabilized blue Convergence Rift
becomes a Stabilized Rift Core. Travel mode never harvests.

A wall-mounted Rift Core Sconce accepts an empty, normal, or stabilized core.
A Stabilized Rift Core creates a passive Rift Ward with a 50-block horizontal
radius and suppresses 97.5% of newly forming natural rifts. It does not remove
existing rifts or interfere with intentional Convergence Rifts.

## Constructed Convergence Gates

**Convergence Gates**

A Convergence Gate contains an authentic blue Convergence Rift inside a reinforced Conflux Iron circuit and links it to a chosen gate for controlled travel.

**Structure**
Build a five-block-wide by five-block-tall outer frame around a clear three-by-three opening. Place one Rift Containment Brace at each of the four corners. Fill the remaining perimeter with eleven Conflux Frame Blocks and one Convergence Core Housing. The Housing replaces the center block on either vertical side and should sit at eye level with its control panel facing outward. Orient the Frame conduits so they follow the perimeter.

**Activation**
Open the Core Housing and install one Stabilized Rift Core and one charged Temporal Crystal with enough energy for a jump. A valid frame powers up in stages, the conduits illuminate, and a contained blue Convergence Rift forms in the opening. Each departure consumes one sixth of full Crystal charge from the departure Gate only: five minutes at the default 30-minute capacity, or six jumps per full Crystal. The receiving Gate pays no arrival cost. Gates do not drain Crystal charge simply by remaining open. Removing either component safely collapses the rift.

**Naming and Linking**
Use the Core Housing to give the gate a recognizable name and select another active gate from the Destination list. Selecting a destination creates the paired link automatically. Both endpoints must remain complete, powered, and available.

**Travel**
Walk into the contained rift to travel to the linked gate. Arrival space is checked on both sides of the destination. If no safe exit exists, travel is blocked and the conduits turn red while the warning pulse circles the frame. Clearing the destination returns the circuit to cyan.

**Access**
The gate owner may set it to Public or Private and list allowed player names. Private destinations accept the owner and explicitly allowed players.

**Indicators**
Dark conduits mean inactive. Cyan conduits and a clockwise cyan pulse mean powered. Red conduits and a faster red pulse mean the linked destination is obstructed.

**Recharging**
Both endpoints must have enough charge to remain powered. A Gate without enough energy for another jump shuts down and retains its Crystal. Remove it through the Housing and top it up in the Rift Resonance Array. Failed arrival refunds the reserved charge. The inventory is briefly locked during transit to keep the charge attached to its Crystal.

**Natural Rift Cores**
A natural Rift Core instead provides Exploration Rift travel and is consumed by that process, returning an empty Containment Core. This is separate from the reusable six-jump Crystal budget for paired Gate travel.


## Rift Resonance Array

**Rift Resonance Array**

A permanent workshop machine for transferring captured rift energy into Temporal Crystals. Craft one controller with eight Conflux Iron plates, six Temporal Glass blocks, six Containment Insulators, six Conflux Iron rods, and one Temporal Gear.

**Placement**
Place at the centre of a clear, dry 5 x 5 area with three blocks of headroom and a solid floor. The control panel faces you. The complete machine is placed together.

**Charging**
Use a station with one depleted or partially charged Temporal Crystal and one natural Rift Core. The Array automatically processes ready stations in clockwise order: three seconds to spin up, a transfer time proportional to the energy supplied, three seconds to spin down, then two seconds to unlock. A full refill always takes sixty seconds of transfer, regardless of the server-configured Crystal capacity; a 50% refill takes thirty seconds and a 10% refill takes six seconds. If the Core has less energy than the Crystal needs, transfer time follows the available Core energy. Small top-ups can finish their transfer in a fraction of a second; alignment and cooldown still take their normal time. A full Rift Core supplies one full Crystal of charge. Top-ups consume only the missing percentage; unused energy remains in the Core. If a Core runs out first, the Crystal keeps the transferred charge. Four Residue are deposited when a Crystal reaches full charge. Only a fully depleted Rift Core becomes an empty Containment Core for reuse. Stabilized Rift Cores power Gates, Sconce wards, and Storm Stabilizers; they cannot charge Crystals in the Array.

**Unloading**
Use an empty hand to remove the Crystal. Sneak-use an empty hand to select the Core instead. The active station stays locked until its cycle finishes; the other stations remain accessible. Look at a station or use the controller to read its status.

**Persistence**
Contents and progress survive saving and reloading. Processing pauses while part of the structure is unloaded. Breaking any part dismantles the Array and returns its contents once; manual survival breaking also returns the controller. Crystals retain their remaining time and Cores retain their unused percentage when removed, saved, placed, or picked up.

**Reading the Machine**
The outer center platform turns clockwise toward the selected station. Its radial lines glow during charging, while the inner rotor spins independently. A glowing Crystal may still have room for a top-up: check its remaining time against full capacity. Core information shows its remaining percentage. The rift and active line glow collapse after the transfer, and the Array advances to the next ready station or returns to idle.

**Residue Tray**
Each Crystal reaching full charge deposits four Temporal Residue in the small base tray near the central rift. Use the tray with an empty hand to collect. An incomplete transfer gives no completion Residue.

Charged Crystals also extend the protective radius of a Temporal Storm Stabilizer.


## Temporal Crystal Charge

**Temporal Crystal**

Condensed temporal energy produced through advanced Temporal Retort research. Review confirmed protocols in Temporal Discoveries or with /rt discoveries.

**Crystal Charge**
A fully charged Crystal holds 30 minutes of energy by default. Item and machine information shows remaining time and available jumps. Server settings can change the full duration. Anchor and paired Gate travel each require one sixth of a full charge: five minutes by default, allowing six jumps from a full Crystal. Charge also spent in a Temporal Drive reduces the jumps available. A partially charged Crystal with less than one jump remaining must be topped up before travel.

**Charging and Appearance**
Use the Rift Resonance Array with a natural Rift Core to charge an empty Crystal or top up a partially charged one. A Crystal with any energy uses the luminous charged model; this does not necessarily mean it is full or has enough energy for a jump. At zero it uses the uncharged model. Remaining energy survives inventory storage, drops, placement and pickup, machine insertion and removal, saving, and Anchor relocation.

**Temporal Drive**
The Drive consumes charge continuously while loaded and running, even without a connected load. It stops at zero and retains the Crystal for empty-hand removal. Time spent paused or unloaded does not drain it.

**Disposable and Reusable Crystals**
An uncharged Crystal powers one Anchor return and is consumed by that jump. A charged Crystal instead spends one sixth of its full capacity per return and remains reusable after depletion. Failed travel refunds reserved charge. Sneak-use the Anchor with an empty hand to remove its reusable Crystal, then recharge it in the Rift Resonance Array. Remove the installed reusable Crystal before inserting another or converting the Anchor to cargo. A partially charged Crystal needs enough energy for a whole jump to be installed.

**Paired Convergence Gates**
Install a charged Crystal beside a Stabilized Rift Core. Each departure spends one jump from the departure Gate only. The receiving Gate must also be powered but pays no arrival cost. A housing retains its depleted Crystal for removal and recharging; failed travel refunds reserved charge.

**Storm Protection**
Install empty or charged Crystals in the four pedestals of a Temporal Storm Stabilizer. Each adds 4 blocks of full-strength radius plus up to 8 more according to its charge, with default settings. Charge is retained during Stabilizer operation; recharge removed Crystals in the Array.


## Temporal Drive

**Temporal Drive**

The Temporal Drive converts energy from an installed Temporal Crystal into mechanical torque using Vintage Story's standard mechanical network. A full Crystal provides 30 minutes of operation by default; the server can configure this duration.

**Placement and Connection**
Place the Drive with its front cartridge facing you. Connect an axle to its mechanical output using normal mechanical placement and connection rules. The Drive may be placed and connected while empty.

**Installing a Crystal**
Use a Crystal with remaining charge on the front cartridge to install it; empty Crystals are rejected. The glass closes, the internal gear and temporal effects activate, and the Drive begins supplying torque. Use the cartridge with an empty hand to retrieve the Crystal; an empty Drive contributes no power or resistance.

**Torque and Speed**
One Drive supplies a modest amount of torque up to its operating speed. Additional Drives connected anywhere on the same mechanical network add their torque together, helping the network carry heavier machinery. Stacking Drives does not directly multiply rotational speed. Use vanilla large and small gears when the network needs a different balance of speed and torque.

**Using a Drive with Wind Power**
A Drive may share a network with a windmill. While the network is below the Drive's operating speed, it assists with torque. If the windmill is already turning the network faster, the Drive freewheels instead of slowing it down. Its position on the connected network does not change this behavior.

**Network Changes**
Adding or removing axles, gears, sails, machines, or Drives causes the vanilla mechanical network to recalculate. A brief adjustment in rotation can be normal while the network settles.

*Multiple Drives increase available torque; gearing determines how that torque is traded for speed.*

**Depletion and Recharging**
Charge drains continuously while the loaded Drive is running, including when no load is connected or the Drive is freewheeling. Time spent paused or unloaded is not charged. At zero, mechanical output, the gear animation, and powered effects stop; the Crystal stays in the cartridge. Use an empty hand to retrieve it. Removal and reinsertion preserve remaining time. Recharge empty or partially used Crystals in the Rift Resonance Array. Hover over the Drive or Crystal to check remaining charge.


## Temporal Storm Stabilizer

**Temporal Storm Stabilizer**
A Conflux multiblock that creates a spherical refuge during temporal storms. Its removable Stabilized Rift Core powers articulated arms and rotating containment rings; four optional Temporal Crystals extend the shield. The visible cyan shell marks the same boundary used for protection.

**Getting the Machine**
This build exposes the controller in Creative inventory. A survival crafting recipe for the Stabilizer is not yet provided.

**Placement and Assembly**
Prepare a clear, dry 9 x 9 footprint with solid support under every floor position. The central 5 x 5 must be clear for five blocks of total machine height, counting the base layer. The four corners require two blocks of total height. Place the controller at the centre; its front faces you. The base extends, conduits and pedestals form, and the central machinery rises through a mechanical and temporal reconstruction sequence. Wait for assembly to finish before installing the core.

**Install the Containment Core**
Right-click the main machine while holding one Stabilized Rift Core. A natural Rift Core or empty Containment Core cannot power it. Stabilized Cores come from capturing a blue Convergence Rift with a prepared Rift Harvester; see Temporal Triangulation and Rift Travel. The core remains removable and is not consumed during operation.

**Controls and Automatic Operation**
With the core installed, the Stabilizer starts automatically during a temporal storm and shuts down when the storm ends. Empty-hand right-click on the main machine manually starts or stops it. Manually stopping during a storm holds off automatic restart for that storm; manually starting again overrides the hold. Outside a storm, manual operation previews the field but provides no storm protection.

To retrieve the core, stop the machine and wait until the rings and arms have fully folded. Then sneak-right-click the main machine with an empty hand. Pedestals have their own interactions, so aim at the central structure for these controls.

**Crystal Pedestals**
Each corner pedestal accepts one Temporal Crystal. Right-click an empty pedestal with a Crystal to install it; right-click an occupied pedestal with an empty hand to retrieve it. Crystals may be empty, partially charged, or full, and can be mixed freely. They retain their charge when removed. The Stabilizer currently does not drain Crystal charge or recharge Crystals. Use a Rift Resonance Array and a natural Rift Core for recharging.

Read the pedestal or item information to check remaining charge. A luminous Crystal is not necessarily fully charged.

**Shield Radius**
At full field strength, default protection extends 16 blocks from the field centre with no Crystals. Each installed Crystal adds 4 blocks even when empty, plus up to 8 more blocks proportional to its charge.

No Crystals: 16-block radius.
Four empty Crystals: 32-block radius.
Four half-charged Crystals: 48-block radius.
Four fully charged Crystals: 64-block radius.
One full, one half-charged, one empty, and one vacant pedestal: 40-block radius.

These are radii, not diameters. Default full-strength radius = 16 + 4 per installed Crystal + 8 times the sum of their charge fractions, capped at 64. Server configuration can change these values. Removing or replacing a Crystal changes the available radius.

The field grows smoothly as it builds strength and contracts as it powers down. During those transitions, only the area inside the current shell is protected. The shield is a complete sphere centred two blocks above the controller base, and also extends below the machine; it is not a flat cylinder or a dome ending at the floor.

**What Protection Does**
Protection requires both an active field and an actual temporal storm. Inside the sphere, personal temporal stability is held at its existing value instead of draining. Low-stability damage and temporal instability effects are suppressed. Storm ambience and visual effects ease away, and the stability gear slows over roughly two and a half seconds. Crossing the boundary plays a sound and a brief temporal particle effect.

This pauses instability; it does not refill stored stability. Leaving the sphere restores normal exposure and your previous stability continues from there. Ordinary weather is not removed.

New hostile spawns, including storm creatures, are prevented inside the active protection zone during the storm. Existing enemies can still enter. The shield is not a solid wall and does not grant general immunity to attacks or projectiles.

**Reading the Machine**
During startup the collar secures the core, the arms deploy, and the segmented rings move into position and rotate. A beam feeds the top of the expanding cyan shell. Particles and branching energy make the boundary visible; stronger storm effects increase the sense of strain. Look at the machine status to confirm that protection is active and read its current radius. A visible field outside a storm is only a preview.

During shutdown, protection contracts with the shell, the rings slow and return to alignment, and the arms fold before the core unlocks. Do not rely on the old boundary while the field is shrinking.

**Saving, Moving, and Troubleshooting**
The machine retains its installed core and Crystals across saving and reloading. It does not keep distant chunks loaded: an unloaded controller cannot protect an area, and incomplete loaded structures pause operation.

If placement fails, check the full footprint, solid support, liquids, and central headroom. If it will not start, finish assembly, install the correct core, and check for a manual stop during the current storm. If the radius is smaller than expected, allow startup to finish and inspect every Crystal charge level. If the core will not come out, stop the machine and wait for folding to finish.

For relocation, shut down and retrieve the contents first. Normal manual breaking of a structure part dismantles the machine and returns its controller and stored contents. Land-claim permissions still apply.

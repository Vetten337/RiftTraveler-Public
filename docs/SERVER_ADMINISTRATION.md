# Rift Traveler Server Administration

## Requirements

- Vintage Story 1.22.6 and 1.22.7 Stable; 1.22.7 is the primary target
- The same Rift Traveler version on server and clients
- One installed Rift Traveler ZIP or folder, never multiple versions

## Useful commands

General player commands:

```text
/rt help
/rt discoveries
/rt recipe
```

Developer and operator commands require `controlserver` privilege:

```text
/rtdev help
/rtdev retort inspect
/rtdev cargo inspect
/rtdev cargo shipments
```

The full Snapshot workflow is documented in
[Snapshot Recipe Maker](SNAPSHOT_RECIPE_MAKER.md).

## Configuration

Rift Traveler server configuration is stored beneath the active Vintage Story
data directory's `ModConfig` area. Do not edit configuration while the server
is running unless a setting explicitly supports live changes.

Generated Retort recipes are stored at:

```text
ModConfig/RiftTraveler/GeneratedTemporalRetortRecipes/
```

They require a restart and never replace packed recipes with duplicate codes.

## Logs

Server logs are normally located beneath:

```text
<VintageStoryData>/Logs/
```

For a server started with `--dataPath ./data`, check:

```text
<server-root>/data/Logs/server-main.txt
```

Include the full startup section and relevant Rift Traveler diagnostics when
reporting a server problem.

## Backups

Rift Traveler is in alpha. Back up world saves before installation, removal,
or updates. Cargo shipment escrow, Anchors, discoveries, and machine state are
stored with the world and should be protected by the same backup policy.


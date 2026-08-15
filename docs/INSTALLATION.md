# Installing Rift Traveler

## Compatibility

The current release is built and tested for Vintage Story `1.22.6 Stable`.
Earlier 1.22.x builds are not officially supported by the 0.3.2 package.
Rift Traveler is required on both the server and every connecting client.

Rustbound Magic integration is optional. When Rustbound Magic is installed,
Rift Traveler adds the Rust Condensation Retort protocol. Rift Traveler remains
fully functional when Rustbound Magic is absent.

## Single-player and client installation

1. Download the Rift Traveler ZIP from the Vintage Story Mod Database.
2. Do not extract the ZIP.
3. Place it in the Vintage Story data `Mods` directory.
4. Remove older Rift Traveler ZIPs or folders.
5. Restart Vintage Story completely.

Typical Windows location:

```text
%AppData%\VintagestoryData\Mods\
```

## Dedicated server installation

Place the same ZIP in the server's active data-path `Mods` directory. A server
started with `--dataPath ./data` normally uses:

```text
<server-root>/data/Mods/
```

Do not leave multiple Rift Traveler versions installed. Restart the server
after changing the package.

## Confirming the mod loaded

After the server has left standby mode, use:

```text
/moddb
```

The startup log should list Rift Traveler among the loaded mods and external
asset origins. If the DLL appears but the items do not, verify that the ZIP
contains forward-slash paths such as:

```text
assets/rifttraveler/itemtypes/temporaltriangulator.json
```

## Updating

Back up the world, stop the game or server, remove the previous Rift Traveler
package, install the new ZIP, and restart. All multiplayer participants should
use the same version.


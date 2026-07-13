# fnvgog2steampatch
Delta patch that turns the executable from the GOG version of Fallout: New Vegas into the one from the Steam version. [Nexus page](https://www.nexusmods.com/newvegas/mods/87244)

## Overview
This delta patch is pretty much only for installing [Begin Again](https://www.nexusmods.com/newvegas/mods/79547) because as far as I know, Begin Again is the only Wabbajack modlist that delta patches platform specific files (4GB patched `FalloutNV.exe`), and as such requires the Steam version.

## Requirements

- [Fallout: New Vegas Ultimate Edition from GOG](https://www.gog.com/en/game/fallout_new_vegas_ultimate_edition)

- [Xdelta3](https://github.com/jmacd/xdelta/releases/tag/latest)

## Installation

1. Extract the contents of the Xdelta3 zip archive to a folder of your choosing (e.g. `C:\xdelta`).

2. Extract `fnvgog2steampatch.xdelta` to the same folder.

3. Open the terminal in this folder.

4. Use the following command to use the patch (replace `<path to game>` with the folder you've installed the game to):
```pwsh
./xdelta3 -d -s "<path to game>\FalloutNV_backup.exe" fnvgog2steampatch.xdelta "<path to game>\FalloutNV_steam.exe"
```
> [!note]
> If you haven't used the [4GB Patcher](https://www.nexusmods.com/newvegas/mods/62552) yet you can use `FalloutNV.exe` instead of `FalloutNV_backup.exe` for the source file.

5. A file called `FalloutNV_steam.exe` should appear in your game's root folder.

6. You should now be able to install Begin Again.

7. After installation, replace the `FalloutNV.exe` located in `<path to where you installed Begin Again>\mods\FNV4GB\Root` with the one from your game's root folder (make sure you've used the [4GB Patcher](https://www.nexusmods.com/newvegas/mods/62552) on it).

> [!tip]
> You can also use this [web app](https://kotcrab.github.io/xdelta-wasm/) if you prefer to use a GUI rather than CLI. You will need to manually place the file `FalloutNV-patched.exe` into your game's root folder.

The output file's hashes should match these:
- CRC-32: `4CE97099`
- CRC-64: `B4FC6DD8F293AC62`
- SHA-1: `d068f394521a67c6e74fe572f59bd1be71e855f3`
- SHA-256: `3a87f92f011e5dc9179ddf733cf08be2b39ea6e5b7a8a9e3a9a72dafcc1b104d`

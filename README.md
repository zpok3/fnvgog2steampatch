# fnvgog2steampatch
Delta patch that turns the executable from the GOG version of Fallout: New Vegas into the one from the Steam version. [Nexus page](https://www.nexusmods.com/newvegas/mods/87244)

## Overview
This delta patch is pretty much only for installing [Begin Again](https://www.nexusmods.com/newvegas/mods/79547) because as far as I know, Begin Again is the only Wabbajack modlist for New Vegas that delta patches platform specific files (4GB patched `FalloutNV.exe`), and as such requires the Steam version.

## Requirements

- [Fallout New Vegas Ultimate Edition from GOG](https://www.gog.com/en/game/fallout_new_vegas_ultimate_edition)

## Installation

1. Extract the contents of the archive your game's root folder.

2. Double click on `FNVGOG2SteamPatcher.bat` or `FNVGOG2SteamPatcher4GB.bat` depending on if you have used the [FNV 4GB Patcher](https://www.nexusmods.com/newvegas/mods/62552) or not.

3. A file called `FalloutNV_steam.exe` should appear in your game's root folder.

> [!tip]
> The output file's hashes should match these:
> - CRC-32: `4CE97099`
> - CRC-64: `B4FC6DD8F293AC62`
> - SHA-1: `d068f394521a67c6e74fe572f59bd1be71e855f3`
> - SHA-256: `3a87f92f011e5dc9179ddf733cf08be2b39ea6e5b7a8a9e3a9a72dafcc1b104d`

4. You should now be able to install Begin Again.

6. After installation, replace the `FalloutNV.exe` located in `<path to where you installed Begin Again>\mods\FNV4GB\Root` with your own 4GB patched executable.

> [!tip]
> Alternatively, you can use the following command (or this [web app](https://kotcrab.github.io/xdelta-wasm/) if you prefer to use a GUI rather than CLI) to use the patch (replace `<path to game>` with the folder you've installed the game to):
```pwsh
.\xdelta3 -d -s "<path to game>\FalloutNV_backup.exe" fnvgog2steampatch.xdelta "<path to game>\FalloutNV_steam.exe"
```

> [!note]
> If you verified your game files because you used the BSA decompressor and haven't rerun the 4GB patch yet, you can use `FalloutNV.exe` instead of `FalloutNV_backup.exe` for the source file.

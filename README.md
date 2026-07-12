# fnvgog2steampatch
Delta patch that turns the executable from the GOG version of Fallout: New Vegas into the one from the Steam version.
## Requirements

- [Fallout New Vegas Ultimate Edition from GOG](https://www.gog.com/en/game/fallout_new_vegas_ultimate_edition) (English version only)

- [FNV 4GB Patcher](https://www.nexusmods.com/newvegas/mods/62552)

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
> If you verified your game files because you used the BSA decompressor and haven't rerun the 4GB patch yet, you can use `FalloutNV.exe` instead of `FalloutNV_backup.exe` for the source file.

5. You should now be able to install Begin Again.

6. After installation, replace the `FalloutNV.exe` located in `<path to where you installed Begin Again>\mods\FNV4GB\Root` with your own 4GB patched executable.

> [!tip]
> You can also use this [web app](https://kotcrab.github.io/xdelta-wasm/) if you prefer to use a GUI rather than CLI.

The output file's hashes should match these:
- CRC-32: `4CE97099`
- CRC-64: `B4FC6DD8F293AC62`
- SHA-1: `d068f394521a67c6e74fe572f59bd1be71e855f3`
- SHA-256: `3a87f92f011e5dc9179ddf733cf08be2b39ea6e5b7a8a9e3a9a72dafcc1b104d`

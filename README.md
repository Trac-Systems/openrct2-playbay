# OpenRCT2 for Playbay

Source code for the OpenRCT2 theme park game that runs on [Playbay](https://playbay.games): a port of
[OpenRCT2](https://openrct2.io) v0.5.5 to the browser, with persistent parks and read-only park visits.

The game code is licensed under the GNU General Public License v3.0 or later (see [LICENSE](LICENSE)).
Upstream projects, libraries, artwork and recordings keep their own licences; per-file notices and
`licences/` inside the archive list them.

## Download

The complete corresponding source is attached to each [release](../../releases) as
`openrct2-playbay-source.tar` (about 740 MB). It contains:

- `project.tar.gz`: the game's code, build scripts, editable artwork and generated exports, tests and locks
- `inputs/`: the checksum-locked upstream source archives and other inputs the build uses
- `SOURCE-MANIFEST.json`: the exact project revision and the hash of every input
- `README.md`: how to restore the inputs and build the game

Check the download against the `.sha256` file published with the release.

## Build

Extract the archive and follow its `README.md`. In short:

```sh
tar -xf openrct2-playbay-source.tar
cd openrct2-playbay-source
tar -xzf project.tar.gz
python3 project/tools/restore_native_source.py --bundle . --project project
cd project
python3 tools/fetch-sources.py
```

OpenRCT2 is a community project and is not affiliated with this port. RollerCoaster Tycoon is a trademark
of its respective owner; no original commercial game data is included or required.

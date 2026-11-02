# WSCart V0.6.0

WonderSwan cartridge emulation

## This fork and integration

This repository is the GimoXagros fork of [FluBBaOfWard/WSCart](https://github.com/FluBBaOfWard/WSCart). `V0.6.0` is the core version in `Version.h`, not a standalone emulator release. This fork has no GitHub Release binaries.

The custom [NitroSwan](https://github.com/GimoXagros/NitroSwan) build pins `source/WSCart` to a specific commit. WSCart also contains the `WSRTC` submodule. Use the emulator's recursive submodule checkout at the selected release tag, following its [development guide](https://github.com/GimoXagros/NitroSwan/blob/main/Docs/DevelopmentGuide.md). The pinned commit can differ from this repository's `main`; do not update it implicitly while reproducing a release.

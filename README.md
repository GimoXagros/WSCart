# WSCart V0.6.0

WonderSwan cartridge emulation

## This fork and integration

This repository is the GimoXagros fork of [FluBBaOfWard/WSCart](https://github.com/FluBBaOfWard/WSCart). `V0.6.0` is the core version in `Version.h`, not a standalone emulator release. This fork has no GitHub Release binaries.

The custom [NitroSwan](https://github.com/GimoXagros/NitroSwan) build pins `source/WSCart` to a specific commit. WSCart also contains the `WSRTC` submodule. Use the emulator's recursive submodule checkout at the selected release tag, following its [development guide](https://github.com/GimoXagros/NitroSwan/blob/main/Docs/DevelopmentGuide.md). The pinned commit can differ from this repository's `main`; do not update it implicitly while reproducing a release.

## RTC protocol correction (2026-11-09)

The WSRTC pin follows the resolution of [upstream PR #2](https://github.com/FluBBaOfWard/WSRTC/pull/2): retain minute carry when correcting invalid seconds and the corrected BCD leap-year calculation. WSCart continues to own the 384,000-clock divider and calls the fork's one-argument `wsRtcUpdate` once per second. RTC structure and saved-state sizes are unchanged. NitroSwan consumes the `agent/nitroswan-dspico-rom-cache-r3` lineage so its ROM-cache hooks remain intact. See the pinned WSRTC README for the correction and validation limits; Alarm/IRQ accuracy is not established by this update.

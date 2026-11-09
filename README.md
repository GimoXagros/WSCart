# WSCart V0.6.0

WonderSwan cartridge emulation

## RTC protocol correction (2026-11-09)

The WSRTC pin follows the resolution of [upstream PR #2](https://github.com/FluBBaOfWard/WSRTC/pull/2): retain minute carry when correcting invalid seconds and the corrected BCD leap-year calculation. WSCart continues to own the 384,000-clock divider and calls the fork's one-argument `wsRtcUpdate` once per second. RTC structure and saved-state sizes are unchanged. NitroSwan consumes the `agent/nitroswan-dspico-rom-cache-r3` lineage so its ROM-cache hooks remain intact. See the pinned WSRTC README for the correction and validation limits; Alarm/IRQ accuracy is not established by this update.

# RVC Dynamic F0 0.1.1 | ready-to-run RTX 40-series

公开下载版本，开发仓库保持私有。This is the fully bundled Windows CUDA 11.8 app, not the earlier minimal installer.

## Download just three files

- **RVC-Dynamic-F0-Open.exe**: click-to-extract launcher.
- **RVC-Dynamic-F0-Windows-cu118.zip.001**: GPU payload, part 1.
- **RVC-Dynamic-F0-Windows-cu118.zip.002**: GPU payload, part 2.

Put all three in one folder, double-click the EXE, and click “Extract and open RVC”. No PowerShell commands, Python/pip setup or model training is required; select your own `.pth` and matching `.index` after opening.

For China-friendly accelerator links, use the table on the [download homepage](https://github.com/whyhea1/rvc-dynamic-f0-downloads#readme). These public downloads require no GitHub login or token; the EXE verifies both payload parts against the original SHA-256 values.

## Included feature

Enable “Dynamic F0” and open “Edit curve” to customize the input-pitch-to-semitone curve, presets, attack/release smoothing and optional pitch ceiling. The curve replaces fixed pitch instead of stacking on top of it, and can be disabled for comparison.

This is a prerelease affecting the desktop realtime GUI only. The source build passed Windows runtime/archive/GUI checks and 39 unit tests, but actual user microphone/GPU latency and voice quality still need testing.

The EXE is unsigned and may trigger SmartScreen. No purchased voice models, personal device configuration, private Git history or credentials are included; retain your original installation.

## Optional files

`START-HERE.md` and `SHA256SUMS.txt` provide instructions and checksums. `RVC-Dynamic-F0-Licenses-and-Sources.zip` provides redistribution notices and corresponding sources; it is not an installation step.

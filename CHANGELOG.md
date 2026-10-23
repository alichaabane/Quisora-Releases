# Quisora changelog

The GitHub Release for each tag remains the authoritative download location and
contains the release-specific notes and `SHA256SUMS.txt`.

## 1.0.0+1 — 2026-10-23

First official Windows release.

- Per-user Windows x64 installer and full-replacement updater.
- Local account dashboard for AI usage and quota information.
- DeepSeek balance reads through the official read-only API.
- Codex usage through the official local CLI companion when connected.
- Usage history, alerts, history retention, system tray behavior and appearance
  settings.
- Software Updates center using this public release channel.

Artifacts:

- `Quisora-x64-1.0.0-1-Installer.exe`
- `Quisora-x64-1.0.0-1-Update.exe`
- `SHA256SUMS.txt`

The packages are unsigned. Automatic in-app installation remains disabled until
a trusted signing/verification mechanism exists.

## Version identity

Tags follow `vMAJOR.MINOR.PATCH+BUILD`, starting with `v1.0.0+1`. The build
number increases for every subsequent delivered package.

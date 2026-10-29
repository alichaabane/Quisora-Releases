# Quisora changelog

## 1.0.0+19 — 2026-10-29

Signed stable Windows x64 release eliminating repeated Command Center projection work.

- About 25× faster in these measured runs: large Codex histories decode in bounded worker isolates instead of blocking the Flutter UI isolate.
- Each account projection is cached; unrelated controller notifications no longer rebuild details and 30-day analytics for every account.
- Account switching renders the cached projection immediately while fresh local data loads.
- Full history, alert accuracy, provider isolation and monitoring behavior are preserved.
- Installer and full-replacement updater preserve existing user data and credentials.
- Ed25519-signed release manifest (`quisora-release-2026-01`); executables are not Authenticode-signed.

## 1.0.0+18 — 2026-10-29

Signed stable Windows x64 release with clearer provider identity and Copilot billing availability.

- Local provider marks include the supplied transparent DeepSeek and OpenAI/Codex images; GitHub, Gemini and hidden future-use Claude marks remain local assets.
- Copilot identity verification is distinct from personal billing access. Empty reports, unsupported rows and reported AI-credit rows stay distinct; 403/404 do not claim Copilot Free or organizational funding.
- Account order can be changed on Accounts and is shared by account menus and dashboard navigation.
- Installer and full-replacement updater preserve existing user data and credentials.
- Ed25519-signed release manifest (`quisora-release-2026-01`); executables are not Authenticode-signed.

## 1.0.0+17 — 2026-10-29

Signed stable Windows release combining provider-confirmed Codex reset success alerts and official personal GitHub Copilot AI-credit billing monitoring.

- Reset success alerts appear in-app and use the Windows notification path after confirmation from fresh provider data.
- Copilot verifies the supplied fine-grained token's account identity and shows personal billing/model consumption. Organization-funded usage, remaining entitlement and reset dates are unavailable; SDK quota access is deferred.
- Installer and full-replacement updater preserve existing user data and credentials.
- Ed25519-signed release manifest; executables are not Authenticode-signed.

## 1.0.0+16 — 2026-10-29

Signed stable release adding read-only Gemini Developer API model metadata and a searchable model catalog. Gemini usage, inference eligibility and remaining quota stay unavailable. File-backed SQLite now runs off the Flutter UI isolate. The installer and full-replacement updater preserve existing user data and credentials.

- Windows x64 installer and updater.
- Ed25519-signed release manifest and detached signature.
- Installer and updater are not Authenticode-signed.

The GitHub Release for each tag remains the authoritative download location and
contains the release-specific notes and `SHA256SUMS.txt`.

## 1.0.0+5 — 2026-10-23

Signed update release adding the Windows startup launch setting.

- Settings → General & Desktop → **Launch Quisora when Windows starts** (HKCU Run).
- Signed manifest and detached signature (`quisora-release-2026-01`).
- Installer and updater packages for `1.0.0+5`.

## 1.0.0+4 — 2026-10-23

Signed update release for the trusted Quisora update chain.

- Ed25519-signed release manifest and detached signature (`quisora-release-2026-01`).
- Installer and updater packages for `1.0.0+4`.
- Installer/updater remain unsigned for Windows Authenticode.

## 1.0.0+3 — 2026-10-23

Trusted baseline release containing the pinned production release public key.

- Install this baseline manually before using in-app signed updates.
- Installer and updater packages for `1.0.0+3`.

## 1.0.0+2 — 2026-10-23

Update Center detection build. No new features.

- Application version `1.0.0+2`.
- Installer and updater packages for Update Center detection testing.
- Packages are unsigned; automatic in-app installation remains disabled.

Artifacts:

- `Quisora-x64-1.0.0-2-Installer.exe`
- `Quisora-x64-1.0.0-2-Update.exe`
- `SHA256SUMS.txt`

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

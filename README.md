# Quisora Releases

**Official Windows release channel for Quisora.**

Quisora is a local-first Windows desktop application for keeping AI account usage
and quotas in one place. It presents provider-reported information without
inventing missing values, keeps accounts separate, and stores credentials in the
operating system's protected storage.

This repository is for **release distribution only**. It contains:

- Windows installer `.exe` files
- Windows updater `.exe` files
- Release notes and version information
- SHA-256 checksums

It does **not** contain Quisora source code, internal documentation, API keys,
authentication files, credentials or user data.

## Download

Latest release: **[Quisora 1.0.0+1](https://github.com/alichaabane/Quisora-Releases/releases/tag/v1.0.0%2B1)**

Use only the assets attached to the official Releases page:

**https://github.com/alichaabane/Quisora-Releases/releases**

Do not use third-party mirrors or links that do not point at this repository's
Releases page.

## Release artifacts

| Artifact | Purpose |
| --- | --- |
| `Quisora-x64-<version>-<build>-Installer.exe` | First-time per-user installation |
| `Quisora-x64-<version>-<build>-Update.exe` | Full replacement update for an existing installation |
| `SHA256SUMS.txt` | SHA-256 digests for the release assets |

Example: `Quisora-x64-1.0.0-1-Installer.exe`.

Requirements:

- Windows 10 or Windows 11, x64.
- Microsoft Visual C++ 2015-2022 Redistributable (x64).

The installer is per-user and does not require administrator rights. Updates
replace application files while preserving data under `%APPDATA%\Quisora` and
credentials stored in Windows Credential Manager.

## Verify a download

Download the release asset and its `SHA256SUMS.txt` from the same GitHub
Release. In PowerShell:

```powershell
Get-FileHash -LiteralPath .\Quisora-x64-1.0.0-1-Installer.exe -Algorithm SHA256
```

Compare the lowercase hexadecimal digest with the matching line in
`SHA256SUMS.txt`. On Windows, `certutil` can also be used:

```powershell
certutil -hashfile .\Quisora-x64-1.0.0-1-Installer.exe SHA256
```

A matching SHA-256 digest confirms that the downloaded file matches the
published checksum. It does not, by itself, prove who published the file. Always
combine it with the official Releases page above.

Quisora does not currently claim production code signing. Windows SmartScreen
may warn when the executables are launched.

## Versioning

Release tags use `vMAJOR.MINOR.PATCH+BUILD`, for example `v1.0.0+1` and
`v1.0.0+2`. The application version is `MAJOR.MINOR.PATCH+BUILD`, and the
build number increases for every delivered package.

Package names encode the same identity using the ADR-040 Windows convention:

```text
Quisora-x64-1.0.0-1-Installer.exe
Quisora-x64-1.0.0-1-Update.exe
```

No version is reserved or published by this repository until a GitHub Release
is created.

## Security

- Download only from this repository's official Releases page.
- Never publish credentials, tokens, authentication files, account data, local
  databases or personal logs in this repository.
- The Quisora source repository and its development material remain private.
- The application's update-checking endpoint is configured in the private
  application source and is not modified by this repository.
- For security reports, use GitHub's private vulnerability reporting for this
  repository when available. Do not include secrets or personal data in a public
  report.

## Release policy

See [RELEASE_POLICY.md](RELEASE_POLICY.md) for the versioning, artifact naming,
checksum and publishing rules. Current release notes are in
[CHANGELOG.md](CHANGELOG.md); per-release checksums are documented in
[checksums/](checksums/).

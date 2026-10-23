# Security

## Download safely

- Download Quisora only from the official Releases page:
  https://github.com/alichaabane/Quisora-Releases/releases
- Verify each executable against the `SHA256SUMS.txt` attached to the same
  release.
- A checksum confirms file integrity, not publisher identity. Do not treat a
  third-party mirror or checksum as official.

## Never share

Do not publish or send any of the following:

- API keys, tokens, passwords or authentication files
- Windows Credential Manager contents
- account databases, usage history or Codex managed homes
- local logs containing personal information

## Reporting a vulnerability

Use GitHub's private vulnerability reporting for this repository when it is
available. If it is not available, do not open a public report containing
sensitive technical details, credentials or user data. The Quisora source
repository remains private; this repository contains release material only.

## Signing status

Quisora does not currently claim a production code-signing identity. Windows
SmartScreen may warn when an unsigned executable is launched. Release notes will
state the actual signing status for every published package. Do not assume that
a checksum match means the publisher has been cryptographically verified.

# Quisora release policy

This repository is the public, release-only distribution channel for Quisora.
It is not a source repository and does not accept application source
contributions.

## Allowed contents

- Windows installer `.exe` artifacts.
- Windows full-replacement updater `.exe` artifacts.
- Release notes and version information.
- SHA-256 checksums for published artifacts.
- This policy, the README, the changelog and checksum documentation.

## Prohibited contents

- Flutter/Dart source code or build projects.
- Internal architecture, task, validation or provider documentation.
- API keys, tokens, passwords, authentication files, signing keys or
  certificates.
- SQLite databases, `auth.json`, `codex-accounts`, pending-reset files, usage
  history, logs with personal data or any other user data.
- Source archives, development builds, debug symbols or test fixtures.

Artifacts belong in a GitHub Release, not in this repository's git history.
The `.gitignore` blocks common binary, credential and user-data files as a
defence in depth; it is not a substitute for checking before publishing.

## Version identity

- Application version: `MAJOR.MINOR.PATCH+BUILD`.
- Release tag: `vMAJOR.MINOR.PATCH+BUILD` (for example `v1.0.0+1`).
- The build component increases for every delivered package. Do not reuse or
  reset a delivered identity.
- The public source of truth for a build remains the private application
  repository's `pubspec.yaml`.

Artifact names use the ADR-040 convention:

```text
Quisora-x64-<MAJOR.MINOR.PATCH>-<BUILD>-Installer.exe
Quisora-x64-<MAJOR.MINOR.PATCH>-<BUILD>-Update.exe
```

Example: version `1.0.0+1` produces:

```text
Quisora-x64-1.0.0-1-Installer.exe
Quisora-x64-1.0.0-1-Update.exe
```

## Checksums

Each release must attach a `SHA256SUMS.txt` file containing one line per
artifact:

```text
<64-lowercase-hex-sha256><two spaces><artifact-file-name>
```

Example:

```text
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa  Quisora-x64-1.0.0-1-Installer.exe
```

The line above is illustrative only. The digest must be computed from the final
packaged file that is uploaded. Do
not reuse a digest from an earlier build.

## Publishing checklist

Only the repository owner performs releases.

1. Build from the private application source using the canonical version.
2. Run the required formatting, analysis, test and Windows release-build checks.
3. Build the installer and updater packages.
4. Compute SHA-256 for both final executables.
5. Create a draft GitHub Release tagged `vMAJOR.MINOR.PATCH+BUILD`.
6. Attach only the installer, updater and `SHA256SUMS.txt`.
7. Write concise release notes using the template below.
8. Verify the uploaded assets and checksums.
9. Publish the release explicitly. A tag alone is not publication.
10. Do not change the application's update-checking endpoint as part of this
    repository's publication work unless that change is separately requested.

## Release notes template

```markdown
## Quisora <version>

### Highlights

- ...

### Downloads

- `Quisora-x64-<version>-<build>-Installer.exe` for a new installation.
- `Quisora-x64-<version>-<build>-Update.exe` for an existing installation.

### Verification

Use `SHA256SUMS.txt` attached to this release.

### Notes and limitations

- Windows 10/11 x64.
- Microsoft Visual C++ 2015-2022 Redistributable (x64) required.
- Signing status: ...
```

## Privacy and source separation

The private `alichaabane/Quisora` repository remains the source of truth for
application code and must stay private. This public repository must never be
used to mirror its source, internal documentation or user data.

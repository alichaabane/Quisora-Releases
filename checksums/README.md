# Release checksums

No release checksums have been published yet. There is no public Quisora release
at this time.

For each published release, download `SHA256SUMS.txt` from the same GitHub
Release as the executables. It contains one line per artifact:

```text
<64-lowercase-hex-sha256><two spaces><artifact-file-name>
```

Verify a downloaded file in PowerShell:

```powershell
Get-FileHash -LiteralPath .\Quisora-x64-1.0.0-1-Installer.exe -Algorithm SHA256
```

Compare the lowercase hexadecimal result with the matching line in the release's
`SHA256SUMS.txt`. A match confirms file integrity against the published
checksum; it does not by itself authenticate the publisher. Use only the
official Releases page:

https://github.com/alichaabane/Quisora-Releases/releases

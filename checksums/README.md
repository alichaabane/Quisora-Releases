# Release checksums

## 1.0.0+2

```text
c108df4d9bdc0bff337dff4214b4a3c807464d3208e9e2373c76c835c968bedf  Quisora-x64-1.0.0-2-Installer.exe
ca4284141376d6ddc9a9af6507f355b21b83ab146670817812a733cc3fa36fae  Quisora-x64-1.0.0-2-Update.exe
```

Release: https://github.com/alichaabane/Quisora-Releases/releases/tag/v1.0.0%2B2

## 1.0.0+1

```text
0a701982bd42a703d267189374d1b3502ee7fd2ce1f2fcaaa76b831590b78a74  Quisora-x64-1.0.0-1-Installer.exe
a17ee38d75fda7ea678e9f4dde0a9e26af60e93f1c0f9cb915cd072b03e12e7f  Quisora-x64-1.0.0-1-Update.exe
```

Release: https://github.com/alichaabane/Quisora-Releases/releases/tag/v1.0.0%2B1

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

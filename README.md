# aria2-static-builds

Automated static builds of [aria2](https://github.com/aria2/aria2) for Windows, macOS, and Linux.

## Highlights

- **All Major Architectures**: Windows (x64 / ARM64), macOS (Apple Silicon / Intel), Linux (x64 / ARM64).
- **Size-Optimized**: Stripped debug symbols (`strip -s`), reducing binary size from ~180MB down to **~4-5MB** (or ~2MB in `.tar.gz`/`.zip`).
- **Fully Automated**: Built via GitHub Actions with pure official upstream source.
- **Integrity Verified**: SHA-256 checksums provided for every release artifact.

## Downloads

Visit [Releases](https://github.com/yxxbc/aria2-static-builds/releases/latest) to download the latest builds for your platform:

| Platform | Architecture | Binary | Archive |
| :--- | :--- | :--- | :--- |
| **Windows** | x86_64 | `aria2c-windows-x64.exe` | `aria2c-windows-x64.zip` |
| **Windows** | ARM64 | `aria2c-windows-arm64.exe` | `aria2c-windows-arm64.zip` |
| **macOS** | Apple Silicon (arm64) | `aria2c-macos-arm64` | `aria2c-macos-arm64.tar.gz` |
| **macOS** | Intel (x64) | `aria2c-macos-x64` | `aria2c-macos-x64.tar.gz` |
| **Linux** | x86_64 | `aria2c-linux-x64` | `aria2c-linux-x64.tar.gz` |
| **Linux** | ARM64 | `aria2c-linux-arm64` | `aria2c-linux-arm64.tar.gz` |

## Verification

Every release includes a `SHA256SUMS.txt` file. You can verify the integrity of the downloaded file:

```bash
# macOS / Linux
sha256sum -c SHA256SUMS.txt

# Windows (PowerShell)
Get-FileHash -Algorithm SHA256 aria2c-windows-x64.exe
```

## License

aria2 is licensed under the [GNU General Public License v2.0 or later](https://github.com/aria2/aria2/blob/master/COPYING).

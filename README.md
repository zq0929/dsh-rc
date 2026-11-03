# dsh-rc

Desktop packages for the **rc** line of
[deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness).

A scheduled workflow follows the newest upstream tag matching
`dsh-v*-rc.*` (currently `dsh-v0.2.1-rc.5`), snapshots its tree, builds three targets,
and publishes them as a GitHub Release:

| Target | Runner | Artifact |
|---|---|---|
| macOS Intel (x86_64) | `macos-15-intel` | dmg + zip |
| macOS Apple Silicon (arm64) | `macos-15` | dmg + zip |
| Windows x64 | `windows-2025` | exe |

- Upstream: https://github.com/deepseek-ai/deepseek-harness (MIT)
- Ordinary repository, not a fork: GitHub disables scheduled workflows in forks.
- Packages are unsigned: macOS is ad-hoc signed and not notarized, the Windows
  installer is unsigned.
- macOS first launch after a browser download:
  `xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"`

# UpdateGit

**Signed installer and auto-updater for Windows apps by [alfonsoautomatiza.com](https://alfonsoautomatiza.com).**

Standalone executable, no dependencies. Download the latest `updategit.exe` from
[Releases](https://github.com/alfonsoautomatiza/updategit/releases/latest).

---

## Usage

```
updategit install <project> [--dir D] [--channel C] [--close a.exe,b.exe]
updategit update <project> | --all
updategit list
updategit --self-update
```

```powershell
updategit install s50bi      # fresh install of the latest version
updategit update --all       # update every installed app (scheduled task)
updategit list               # installed apps and versions
```

- Downloads only from the Ed25519-signed manifest published at
  `https://alfonsoautomatiza.github.io/releases/<project>/manifest-stable.json`.
- Every package is checked against the signed size and SHA-256 before it is applied.
- Updates are atomic: if anything fails, the previous installation is restored.
- Default install folder: `C:\ALCATIC\<project>`.
- Exit codes: `0` ok, `1` install/update failed, `2` usage error.

---

**© 2026 [alfonsoautomatiza.com](https://alfonsoautomatiza.com)**

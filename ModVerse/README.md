# ModVerse Runtime Assets v2

Upload **ModVerse_Runtime_v2.zip**, **manifest.json**, and **README.md** directly into:
`GTAV-Cherax/ModVerse/assets/`

This package contains **six native runtime DLLs only**. No `.cmd`, `.ps1`, `.exe`, diagnostic `.asi`, user settings, installed mods, caches, or external worker.

**Future first-run experience:** Put a single ModVerse Lua script into Cherax/Lua, load it, and let the Lua script fetch this pinned runtime ZIP from GitHub, verify its SHA-256 against a checksum embedded in the Lua release, extract to `Cherax/Lua/ModVerse/runtime/native/`, and continue automatically. The first-run downloader is NOT provided by this asset package alone. Build 072 currently bundles these DLLs locally.

**Archive limitation:** Existing RAR/7Z worker support still requires launching a separate PowerShell process. These six DLLs do not magically replace the worker. A separate tested in-process archive library would be required for zero-manual-step RAR/7Z, or ModVerse can support ZIP and leave RAR/7Z as optional/unsupported. Do not remove the worker from existing builds yet if relying on RAR/7Z downloads.

**Security:** Audit and confirm redistribution rights for each binary before making a public GitHub release. GitHub upload is not automated by this package.

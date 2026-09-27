# Zombombo Game Builds

This public repository hosts game builds for the Zombombo updater. The updater downloads the latest stable GitHub Release, verifies `game.zip.sha256`, and installs `game.zip`.

## Publish a build

A collaborator with write access can download `Publish-GameBuild.ps1` from this repository, sign in with `gh auth login`, then run:

```powershell
.\Publish-GameBuild.ps1 -BuildDirectory 'C:\Game\Build' -Version 'v1.0.0'
```

The script creates `game.zip` and its SHA-256 checksum and publishes a normal Release. Put the game files directly in the build directory so they appear at the ZIP root. Use a new version tag for every build.
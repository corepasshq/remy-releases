# Remy Releases

Public download channel for the **Corepass Remy** desktop app.

This repository contains no source code. Installers are attached as assets to
[GitHub Releases](https://github.com/corepasshq/remy-releases/releases).

## Download

1. Open the [Releases page](https://github.com/corepasshq/remy-releases/releases).
2. Choose a release:
   - **Latest** is the current stable release.
   - **Pre-release** (`vX.Y.Z-rc.N`) builds are release candidates. They
     connect to production Remy services.
3. Download the installer for your platform from **Assets**.

## Platforms

| Platform            | Notes                |
| ------------------- | -------------------- |
| macOS Apple silicon | Signed and notarized |
| macOS Intel (x64)   | Signed and notarized |
| Windows x64         | Unsigned installer   |
| Linux x64           | Unsigned AppImage    |

Each release lists the platforms it supports under **Availability** in its
notes. Some releases are macOS only. For example, `v0.3.3` has no Windows or
Linux installers.

### Unsigned builds

- **Windows:** SmartScreen may warn that the publisher is unknown. Choose
  *More info → Run anyway*.
- **Linux:** make the AppImage executable before you run it:

  ```sh
  chmod +x <downloaded-file>.AppImage
  ./<downloaded-file>.AppImage
  ```

## Versioning

- Stable releases use the tag `vX.Y.Z`.
- Release candidates use the tag `vX.Y.Z-rc.N`, and GitHub marks them as
  pre-releases.

## How releases are published

- The **Build Desktop** workflow in `simple-coding-harness` builds the
  installers and publishes them here automatically.
- macOS Intel (x64) `.dmg` files are built locally and uploaded by hand.
- Release notes come from `remy-desktop/docs/release-notes/` in the source
  repository. Each release body ends with a hidden `remy-release-notes`
  metadata comment that records the source commit and a SHA-256 checksum of
  the notes.

## Reporting issues

This repository only distributes the installers. Report app bugs and feature
requests through the main Remy project, not here.

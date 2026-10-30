# DOSVBox roadmap

This is a proposed feature plan. Items below are not implemented merely because they appear in this document.

## Security and trust

- [x] Add a security guide with realistic limitations and least-privilege recommendations.
- [x] Run scheduled and pull-request CodeQL analysis for the C++ codebase.
- [ ] Add a per-game profile manager that stores each game's configuration separately.
- [ ] Add a restricted-folder launcher that mounts only a selected game directory.
- [ ] Add optional network-off presets for new profiles.
- [ ] Publish SHA-256 checksums and a software bill of materials for every release.
- [ ] Sign official Windows installers when a verifiable code-signing certificate is available.

## User experience

- [ ] Add a game library with custom names, icons, and per-game settings.
- [ ] Add one-click launch and recent-game history.
- [ ] Add screenshot and capture shortcuts with an in-app gallery.
- [ ] Add configuration backup and restore.
- [ ] Add a first-run setup wizard and accessible light/dark themes.

## Compatibility

- [ ] Keep DOSBox Staging compatibility as the priority.
- [ ] Add automated regression tests for any new launcher or profile features.
- [ ] Preserve upstream attribution, licensing, and notices in source and binary distributions.

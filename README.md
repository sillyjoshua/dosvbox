# DOSVBox

DOSVBox is a security-focused community build of [DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging), intended to make running classic DOS software safer and easier on modern systems.

The emulator core is based on DOSBox Staging. This repository retains the upstream project's GPL-2.0-or-later licensing and notices; see [LICENSE](LICENSE) and the bundled `licenses/` directory.

## Security-first usage

- Run DOSVBox as a standard Windows user; it does not need administrator rights for normal use.
- Keep DOS games and applications in a dedicated folder, and mount only that folder when possible.
- Use DOSBox's `securemode` setting for sessions where you do not need to change mounted drives from inside the DOS shell.
- Leave emulated networking disabled unless a particular program needs it.
- Treat DOS executables and disk images from unknown sources as untrusted. The emulator is not a complete operating-system sandbox.
- Download builds only from this repository's Releases and verify published SHA-256 checksums when available.

See [DOSVBox security guide](docs/DOSVBOX-SECURITY.md) for the threat model and setup guidance.

## Security checks

Pull requests and pushes to `main` are scanned with GitHub CodeQL for C++ security issues. The workflow runs independently from the existing Windows build workflow.

## Upstream project

DOSVBox builds on DOSBox Staging, a modern continuation of DOSBox. Please retain upstream copyright notices and comply with the GPL when distributing modified binaries or source.

- [DOSBox Staging upstream](https://github.com/dosbox-staging/dosbox-staging)
- [DOSBox Staging documentation](https://www.dosbox-staging.org/)
- [License](LICENSE)

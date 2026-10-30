# DOSVBox security guide

## Security goals

DOSVBox aims to reduce avoidable risk when running legacy DOS software. It adds security-focused project guidance and automated source analysis; it does **not** turn DOSBox into a hardened virtual machine or guarantee that hostile DOS programs cannot affect the host.

## Recommended Windows setup

1. Install DOSVBox in a normal user-writable location. Do not run it as Administrator.
2. Create a dedicated directory for DOS software, for example `%USERPROFILE%\\DOSVBox\\Games`.
3. Keep downloads and disk images from unknown sources separate until scanned and reviewed.
4. Mount only the specific game directory you need, rather than your whole user profile, Desktop, Documents, or system drive.
5. Avoid mounting folders that contain credentials, browser profiles, SSH keys, source-code secrets, or personal documents.
6. Disable emulated networking unless the game or application explicitly requires it.
7. Back up save files. Treat save files and disk images as untrusted input too.

## DOS secure mode

DOSBox Staging provides a DOS `securemode` setting. Enable it for sessions where you do not need DOS shell commands that change drive mounts or other protected configuration. Consult the configuration reference shipped with this exact DOSVBox build for the supported syntax and behaviour. Secure mode is an emulator-level restriction, not a Windows sandbox.

## Important limitations

- DOSBox runs as your Windows user. A DOS program may be able to read or modify files in directories you mounted and may exploit bugs in the emulator or its dependencies.
- A restricted mount is useful least-privilege practice, but it is not equivalent to a separate VM, Windows Sandbox, or an OS-enforced sandbox.
- Disabling emulated networking reduces exposure but does not replace host firewall controls.
- No build can be guaranteed to avoid Microsoft Defender detections. Do not disable Defender or add exclusions to make a build run. Report suspected false positives to Microsoft and provide the exact release hash.

## Reporting a security issue

Please use GitHub's private vulnerability reporting for this repository where available: <https://github.com/sillyjoshua/dosvbox/security/advisories/new>. Do not publish exploit details in a public issue before maintainers have had a chance to assess the report.

## Build integrity

- Build from source using the documented Windows build instructions.
- Review dependency changes and keep vcpkg dependencies updated.
- Use the repository's CI results before distributing a build.
- Publish SHA-256 hashes alongside release archives and installers.
- Code signing can help identify the publisher and detect tampering, but requires a legitimate signing certificate and does not guarantee a clean Defender verdict.

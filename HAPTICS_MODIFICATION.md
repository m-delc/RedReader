# Optional haptic feedback (fork modification)

RedReader > Settings > Behaviour > Haptic feedback defaults to **off** in this fork.

The implementation disables Android View-level haptic feedback in activities derived from `BaseActivity`, including newly laid-out views. Turning the setting on restores each tracked view's original haptic-enabled state.

## Scope and limitations

This does not suppress direct `Vibrator` calls, system navigation haptics, or haptics produced by the keyboard or other apps. Verify behavior on an actual GrapheneOS device.

## Building

The existing GitHub Actions CI workflow (`.github/workflows/build.yml`) assembles release and debug builds, uploads the debug APK, and runs static checks and tests. A fork-signed debug APK may not be installed over the official app because signatures differ. Back up app settings before replacing an existing installation.

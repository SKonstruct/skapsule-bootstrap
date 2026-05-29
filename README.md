# skapsule-bootstrap

Platform-independent Java bootstrap code for launching the Spiral Knights client via getdown.
Shared as a submodule across [SKapsule](https://github.com/SKonstruct/SKapsule) (Android) and [SKapsule-iOS](https://github.com/SKonstruct/SKapsule-iOS).

## Contents

- **`SkBootstrap.java`**: Configures SK's classpath, env, properties, and cacio bridge.
- **`HeadlessGetdown.java`**: Headless driver for getdown to download SK assets.
- **`NativeBridgePrompt.java`**: Implements frenchpress `CredentialPrompt` via the JNI/Block native bridge.
- **`GLFW.java`**: Custom GLFW shadow implementation bridging LWJGL to native touch/input systems.

## Integration

### Android (SKapsule)
Included via `settings.gradle.kts` and built by Gradle (`build.gradle.kts`).

### iOS (SKapsule-iOS)
Built directly into `sk-bootstrap.jar` via `scripts/build-bootstrap.sh`.

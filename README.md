# Darkest Fear Android — build project

This repository is intended to build a **standalone Android APK** for the supplied Java ME MIDlet using the `midlet` product flavor of [J2ME-Loader](https://github.com/nikita36078/J2ME-Loader).

## Build status

This is source/build automation, **not a precompiled APK**. The workflow must run in GitHub Actions and the resulting APK must be installed and tested on an Android device before it can be called finished.

## Build on GitHub

1. Upload the contents of this folder to the root of your GitHub repository (keep the `.github/workflows` folder and the `game` folder).
2. In the repository, open **Actions** and enable workflows if GitHub asks.
3. Run **Build Darkest Fear Android APK** (or push a commit to `main`).
4. Open the completed workflow run and download the artifact `Darkest-Fear-Android-debug-apk`.
5. Extract the APK and install it on Android. Test launch, touch controls, sound, saves, and orientation.

## Original MIDlet

- Name: Darkest Fear
- Entry point: `RMIDlet`
- Version: 1.19
- Profile: MIDP 1.0 / CLDC 1.0

## Important caveat

A successful Gradle build is not proof that gameplay works. If the workflow fails, the Actions log is needed to correct the exact build issue. If the APK builds but does not start, runtime compatibility and resource loading must be debugged on-device.

The original game JAR, artwork, and trademarks remain the property of their respective owners. The J2ME-Loader runtime is licensed under Apache-2.0.

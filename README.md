# Avocado — Fabric client starter

This is an independent starter project for Minecraft 1.21.11 / Java 21, based on the user's requested Avocado branding.

## Included in this starter
- New Fabric mod ID/name: `avocado` / `Avocado`.
- A basic ClickGUI opened with **Right Shift**.
- Category tabs and on/off switches for the initial module registry.
- A JSON config saved to `.minecraft/config/avocado.json`.
- The generated horror avocado loading artwork bundled as `assets/avocado/textures/gui/loading.png`.
- A reference catalog containing the 62 module IDs and default settings read from the supplied Anubis 0.9.9.3 JAR.
- UI branding text `King & Donut`.

## Important limitation
This is **not** a feature-complete clone of Anubis. The listed module switches are UI placeholders; the original combat, ESP, movement, Donut automation, radar, and other game hooks have not been reimplemented. The loading artwork is bundled but not yet connected to Minecraft's loading overlay. The original JAR is signed and contains a pre-launch integrity check, so this project does not modify or disable that protection.

## Build
Open this folder in a Java 21 / Gradle environment and run:

```sh
./gradlew build
```

The first build requires internet access to resolve Fabric Loom, Minecraft, mappings, and Fabric API. Dependency versions are pinned in `gradle.properties`; if Fabric's repository has moved versions, update them there.

## Next implementation phase
Implement each module as a separate class using Fabric events and supported Minecraft APIs, then connect the loading texture to a supported loading-screen hook. Do not copy protected Anubis internals or bypass its integrity verification.

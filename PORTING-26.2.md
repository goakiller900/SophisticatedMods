# Minecraft 26.2 Fabric port

This branch coordinates the Minecraft 26.2 port of the Fabric versions of Sophisticated Core and Sophisticated Backpacks.

## Active repositories

- `goakiller900/SophisticatedCore` — branch `agent/port-26.2`
- `goakiller900/SophisticatedBackpacks` — branch `agent/port-26.2`
- `goakiller900/SophisticatedMods` — branch `agent/port-26.2`

Sophisticated Storage is not part of the initial port scope.

## Verified 26.2 toolchain

- Minecraft `26.2`
- Java `25`
- Gradle `9.5.1`
- Fabric Loom `1.17-SNAPSHOT`
- Fabric Loader `0.19.3`
- Fabric API `0.154.2+26.2`

Minecraft 26.2 is unobfuscated. The port builds therefore do not configure Mojang or Yarn mappings.

## Build order

1. Compile and port Sophisticated Core.
2. Build a local Sophisticated Core development jar.
3. Compile Sophisticated Backpacks against that jar.
4. Restore optional integrations individually after the base mods compile and launch.

## Current known blocker

The 1.21.1 Fabric port depends on several Porting Lib modules and other compatibility libraries that do not yet provide a direct Minecraft 26.2 upgrade path. The diagnostic builds intentionally start with Minecraft, Fabric Loader, and Fabric API only so compiler output can identify the exact compatibility surface that needs replacing.

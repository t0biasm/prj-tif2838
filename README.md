# prj-tif2838

Software for the TI TMDSCNCD28P65X evaluation board (TMS320F28P65x, C2000) with FreeRTOS.

| Path | Content |
|---|---|
| `applications/tif2838` | Application, units, linker scripts (see its README and `swArchitecture.puml`) |
| `emb-toolchain` | submodule: [emb-toolchain](https://github.com/t0biasm/emb-toolchain), compilers and tooling |
| `emb-platform` | submodule: [emb-platform](https://github.com/t0biasm/emb-platform), MCU platform code incl. FreeRTOS port |
| `emb-platform/c2000/freertos/upstream` | nested submodule: TI FreeRTOS kernel (`REL_C2000Ware_v5.05.00.00`) |

## Getting started
```
git clone --recurse-submodules https://github.com/t0biasm/prj-tif2838.git
```
Create `user.bazelrc` (gitignored) with the Artifactory URL the compilers are downloaded from:
```
common --repo_env=EMB_ARTIFACTORY_URL=https://<host>/artifactory
```
Compiler downloads authenticate via `~/.netrc`. Then:
```
bazel build --config=c2000 //applications/tif2838/swe/app:app
```
The project's `FreeRTOSConfig.h` is selected in `.bazelrc` (`--@emb_platform//c2000/freertos:config=...`).

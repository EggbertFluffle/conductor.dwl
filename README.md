# conductor.dwl

Conductor.dwl is an implementation of the [Conductor](https://github.com/EggbertFluffle/Conductor) DSL, a language designed to unify how we describe dynamic window management.

## Patching

This plugin is for [dwl](https://codeberg.org/dwl/dwl). Once you have your dwl source code, patch the `conductor.diff` to your source. You will also need the [Conductor](https://github.com/EggbertFluffle/Conductor) binary built for your system. We do not package prebuilt binaries.

```sh
curl {URL_GOES_HERE} ./conductor.diff
patch < conductor.diff
make clean install
```

## Configuration

Below is the default configuration. Make sure to assign your conductor binary path to `CONDUCTOR_BIN_PATH`.

```c
const char* CONDUCTOR_BIN_PATH = "/your/conductor/bin/path/here";
const char* CONDUCTOR_STARTING_VARIABLE = "start";
const char* CONDUCTOR_SNIPPET = "start = full [|] ?stack\\nstack = full (-) stack";
const double CONDUCTOR_MAX_DEPTH = 25.0;
```

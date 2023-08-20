---
description: (NOT IMPLEMENTED)
---

# Build scripts

Build scripts in Grill are self-contained projects inside your package used for preparing the package upon installation or rebuild. For example to build a system library.&#x20;

The buildscript must be a grill package.

```toml
...
[Buildscript]
Path = "./Buildscript"
```

A useful package for cloning git submodules and/or building using CMake is [BuildTools](https://grillpm.vercel.app/package/BuildTools).

You can rebuild your package using the [rebuild](../commands/rebuild.md) command.

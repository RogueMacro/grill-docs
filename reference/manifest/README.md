# Manifest

The manifest is the <mark style="color:yellow;">`Package.toml`</mark> file in every package. It contains all the information Grill needs to know about your package. A minimal manifest requires three fields. <mark style="color:orange;">`Name`</mark>, <mark style="color:orange;">`Version`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> and <mark style="color:orange;">`Description`</mark>. For example:

```toml
[Package]
Name = "MyProject"
Version = "0.1.0"
Description = ""
```

## Dependencies

Dependencies are added to a <mark style="color:orange;">`[Dependencies]`</mark> table in the manifest. There are 3 types of dependencies:

* Registry
* Git
* Local

### Registry

Registry dependencies are the standard way of specifying dependencies. Here the identifier is a published package with a version requirement. The version requirement can be any semver-compatible string.

```toml
...
[Dependencies]
OpenGL = "3.3.0"
```

You can specify which features you want to enable for that specific dependencies with a feature array:

```toml
...
[Dependencies]
ImGui = { Version = "1.88", Features = ["OpenGL", "GLFW"] }
```

A package might have some default features enabled. You can disable these with the <mark style="color:orange;">`DefaultFeatures`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> bool.

```toml
...
[Dependencies]
ImGui = { Version = "1.88", DefaultFeatures = false }
```

### Git

Git dependencies require a url and a revision. They are not taken into account when resolving, so types from those dependencies cannot be passed to other dependencies safely.

```toml
...
[Dependencies]
OpenGL = { Git = "https://github.com/opengl/opengl", Rev = "f478h29d" }
```

### Local

Local dependencies are specified by path.

```toml
...
[Dependencies]
MyUtilities = { Path = "./path/to/project" }
```

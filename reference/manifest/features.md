# Features

You can add features to your package with the <mark style="color:orange;">`[Features]`</mark> section in the package manifest.

```toml
...
[Features]
Default = ["Docking"]
GLFW = "GlfwProject"
OpenGL = "OpenGLProject"
Docking = []
WindowAndRendering = ["GLFW", "OpenGL"]
```

Let's break this down.

First, the <mark style="color:orange;">`Default`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> feature specifies the features that should be enabled by default.

The <mark style="color:orange;">`GLFW`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> and <mark style="color:orange;">`OpenGL`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> features are two separate projects inside the package (The projects are technically packages too, since they require a manifest). When these features are enabled by a dependent, those projects will be added to the workspace and as dependencies to the dependent.

The <mark style="color:orange;">`Docking`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> feature maps to no project, and currently does nothing. In a future release all enabled features will emit a <mark style="color:blue;">`FEATURE_...`</mark> pre-processor macro. The <mark style="color:orange;">`Docking`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> feature would in that case emit a <mark style="color:blue;">`FEATURE_DOCKING`</mark> <mark style="color:blue;"></mark><mark style="color:blue;"></mark> macro.

The <mark style="color:orange;">`WindowAndRendering`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> feature enables the <mark style="color:orange;">`GLFW`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> and <mark style="color:orange;">`OpenGL`</mark> <mark style="color:orange;"></mark><mark style="color:orange;"></mark> features.

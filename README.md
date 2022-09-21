# Getting Started

Download and install the latest release of Grill from \[GitHub]\(https://github.com/roguemacro/grill/releases/latest).

## Creating a new project

Run `grill new MyProject` to create a new console application.

Inside the newly created `MyProject` directory, we run the [make.md](commands/make.md "mention") command:

```
$ grill make
        Make MyProject v0.1.0

       [1/4] 🧭 Up to date ✔
       [2/4] 🔍 Resolution ready ✔
       [3/4] 🚚 Packages on disk ✔
       [4/4] 📦 Workspace done ✔
             🍝 Enjoy your spaghetti!
```

Now you should have a Beef workspace that you can open in your IDE.

## Initializing an existing project

To initialize an existing project, make sure your main project is at the root of your package. Then run `grill init` to add the necessary files for a Grill package. You can use the [make.md](commands/make.md "mention") command to generate the workspace.

\*Note:\* Generating a new workspace will remove any dependencies \*not\* listed in the manifest. Remember to add your dependencies to the manifest before you run `grill make`.

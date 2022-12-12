
## How to configure debug launch arguments

Visual Studio's Open Folder mode allows configuring the
arguments for a debugger launch using a `launch.vs.json`
file.  This file can be placed in the `.vs` directory,
or, as in this example, as a sibling to `Cargo.toml`.

```
{
  "version": "0.2.1",
  "defaults": {
  },
  "configurations": [
    {
      "type": "default",
      "name": "Bin: debug_launch_args/debug_launch_args",
      "project": "Cargo.toml",
      "projectTarget": "debug_launch_args/debug_launch_args/bin",
      "args": 
      [ 
          "--flag",
          "value"
      ]
    }
  ]
}
```

- `type` must be "default"
- `projectTarget` is the three things, separated by slashes: the name of the package, the name of the target, and the kind of the target.
- `project` must be "Cargo.toml"
- `name` must be the name as it appears in the dropdown control in the toolbar.
- `args` is a json array of strings, which will be the arguments passed to the executable being debugged

The `launch.vs.json` feature is documented at:

https://learn.microsoft.com/en-us/visualstudio/ide/customize-build-and-debug-tasks-in-visual-studio?view=vs-2022

If you right-click on a target in Rust View and choose "Open Debug and Launch Settings", it will bring up the `launch.vs.json` file, and all of the fields except `args` should be pre-filled correctly.



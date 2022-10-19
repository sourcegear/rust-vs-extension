
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
      "projectTarget": "debug_launch_args/debug_launch_args",
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
- `projectTarget` is the name of the package and the name of the target, separated by a slash
- `project` must be "Cargo.toml"
- `name` must be the same as projectTarget, except with "Bin: " or "Example: ", to indicate what kind of target.  Note the space after the colon.
- `args` is a json array of strings, which will be the arguments passed to the executable being debugged


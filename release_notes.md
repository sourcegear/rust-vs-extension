# Release notes

SourceGear Rust is an extension for Visual Studio 2022.

- Intellisense features (using rust-analyzer)
- Syntax coloring for .rs and .toml
- Build, Clean, etc
- Debugging
- Rust View, showing Cargo package/target/dependency hierarchy
- Template to create a new project
- Manage the installation of Rust tools from within Visual Studio

For a more detailed overview, see [Getting Started](getting_started.md).

All versions prior to 1.0 will be marked as Preview.

The 1.0 release (coming soon) is intended to be a "Minimum Viable Product",
suitable for production use, and a stable foundation on which to build
more features.

In the future, probably in the 2.0 time frame, we plan to offer both 
free and commercial editions of this extension.

## 0.8 -- (9-January-2023)

Although this remains a "Preview", we are finding it
generally satisfactory for regular development work.

We will be focused on bug fixes and polishing from
here until 1.0.  Feedback is welcome.

Changes in this preview release:

- Support for Rust language options and the "map mode" scrollbar
- Obtain (and update) rust-analayzer from rustup
- Improvements to the handling of messages in Error List
- Various improvements to 'rustup' UI features
- Other bug fixes and performance improvements

## 0.7 -- (9-December-2022)

This extension remains far from polished, and is not yet feature complete,
but we are now able to use it productively in actual Rust development work.

Changes in this preview release:

- The bundled copy of rust-analyzer has been updated
- The project template feature has been brought back
- New 'rustup' features to manage the installation and updates of Rust tools
- Integration with Test Explorer has been removed, for now
- Added a dropdown to the toolbar to configure profile for Build All
- Lots of bug fixes

## 0.6 -- (18-October-2022)

Still rough.  Released to show direction and progress:

- Use Visual Studio's Open Folder mode
- Rust View, showing Cargo package/target/dependency hierarchy
- Show Rust compiler error messages in Visual Studio Error List
- Support for cargo workspaces with multiple packages
- Initial integration of Cargo tests with Test Explorer
- Comment/Uncomment for Rust code in editor
- Project template features temporarily removed
- No longer requires admin privileges to install

## 0.5 -- (04-August-2022)

Initial public preview release, with a very basic feature set:

- Intellisense features (using rust-analyzer)
- Project file (`.rsproj`) wrapping `Cargo.toml`
- Build, Rebuild, etc
- Debugging
- Syntax coloring for `.rs` and `.toml`
- Templates for new Rust projects
- Open existing `Cargo.toml` as a project


# Getting Started

## Install the extension

SourceGear Rust is available in the Visual Studio
Marketplace.  It is compatible with Visual Studio 2022
for Windows, including the Community, Professional, or Enterprise editions.  
Other products in the Visual Studio family
(Visual Studio for Mac, Visual Studio Code) are not supported.

The download for SourceGear Rust is a single file with
a name ending in `.vsix`.  This kind of file is the standard format for 
Visual Studio extensions, and such a file is often referred to as "a VSIX", 

One way to install SourceGear Rust is to download the VSIX
from the Visual Studio Marketplace website:

https://marketplace.visualstudio.com/

Close Visual Studio itself, and then open the VSIX file, which will bring up 
the VSIX Installer.  This will configure the extension for your installation
of Visual Studio.

Another approach is to use the Manage Extensions feature
within Visual Studio.  If you install a VSIX from there, it will be
scheduled for install, and The VSIX Installer will be launched after
you close Visual Studio.

Either way, after the VSIX is installed, the Rust features should
be available the next time you launch Visual Studio.

## Install the Rust development tools

The current version of SourceGear Rust expects
the Rust development tools to be installed separately.
These tools include the Rust compiler and its package
manager (Cargo) and various other things to support 
development with Rust.

The standard tool for managing a Rust installation
is called `rustup`:

https://rustup.rs/

SourceGear Rust will look for the Rust tools to be installed
at the default location, which is `$(UserProfile)\.cargo\bin\`.

## About Rust projects in Visual Studio

Visual Studio users are familiar with the notion of a "project file".
For example, C# developers have project files ending in `.csproj`,
and C++ developers have project files ending in `.vcxproj`.
These files use "MSBuild", the underlying build system for
Visual Studio.

For Rust projects, we create a project file ending in `.rsproj`,
but the contents of this file are very simple.  It basically
looks like this:

```
<?xml version="1.0" encoding="utf-8"?>
<Project Sdk="SourceGear.Rust">
</Project>
```

And the reason this file is simple is because all it really 
does is delegate all the work to Cargo.

Key point:  SourceGear Rust does not replace `Cargo.toml` or duplicate
its contents-- it merely provides a "wrapper" around it.

## Create a new project from a template

Like most language integrations for Visual Studio, SourceGear Rust includes 
several project templates which can be used from the "Create a new project"
dialog.  That dialog offers a way to filter by programming language,
and if you choose Rust from that dropdown control, you will see the
available templates.

These templates will create a `Cargo.toml` file for you.

## Open a Cargo.toml file as a project

If you already have a `Cargo.toml` file,
you can simply open it as a Visual Studio project.
SourceGear Rust will automatically create an adjacent `.rsproj` file.


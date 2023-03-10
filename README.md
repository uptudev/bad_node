# bad_node

*bad_node* is a technological horror game. It is still wholly a WIP and should not be run on anyone's computer before a v1.0.0 release, as it will mostly serve as my first proper attempt at game development without a commercial game engine.

## Installation

Until a full release version is ready, any binaries on this site will be provided only for my native dev environment of x64 Linux. I cannot guarantee any stability for other OSes, although the following instructions will detail the building process for compiling Rust source code into binaries.

### Installing Rust

Rust is unfortunately not native on any OSes (that I know of), so you must download the compiler before you can build the binaries.

#### Unix (Linux/macOS)

To install the Rust package manager, `cargo`, use the following command:
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

This will download an install script from [rustup](https://rustup.rs/), which will then run and install Cargo on your system.

#### Windows

To install Rust on Microsoft Windows, [download the installer](https://win.rustup.rs/) from [rustup](https://rustup.rs/). 

#### Other OSes

For any other unmentioned OSes, please see the Rust documentation [here](https://forge.rust-lang.org/infra/other-installation-methods.html#other-ways-to-install-rustup) for other platforms' versions of `rustup-init`.

### Downloading and Building **bad_node**

#### Unix (Linux/macOS)

To build the most up to date version, use `git` to pull from the repository with the following set of commands, which can be put into a `.sh` file for ease of use. Please keep in mind that this script currently deletes anything in your `~/bad_node` folder. If you've already cloned the repository using this script, use `git pull` instad.
```sh
cd ~
rm -rf ./.bad_node
mkdir ./.bad_node
git clone https://github.com/uptudev/bad_node ./.bad_node
cd ./.bad_node
cargo build
```

#### Windows

I am very unfamiliar with PowerShell, so this script may not work at all; in that case, just download the source code as a .zip or tarball and extract it to the \Program Files\bad_node\ directory, then build with `cargo build` after changing the working directory to the extracted archive.
```powershell
winget install git
rm -r $Env:Programfiles\bad_node\
mkdir $Env:Programfiles\bad_node\
git clone https://github.com/uptudev/bad_node $Env:Programfiles\bad_node\
cd $Env:Programfiles\bad_node\
cargo build

```

#### Other OSes

Install via downloading the source code archive of the newest release of the repo, then extract the archive and run `cargo build` in the extracted archive.

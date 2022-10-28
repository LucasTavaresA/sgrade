# sgrade

Simple alternative to [topgrade](https://github.com/topgrade-rs/topgrade)

or Suckless, Shellscript... maybe S tier

## Install

Put sgrade in your `PATH`, or execute:

```shellscript
git clone https://github.com/lucastavaresa/sgrade
./sgrade/sgrade
```

## Update Steps

sgrade have all steps enabled by default, but even when enabled
it does not update resources you don't have

You can change what updates and the order by setting `SG_RESOURCES`
to the resource names separated by space, like: `packages etc cargo`

| Resource   | Description                                                                                                            |
|:----------:|:-----------------------------------------------------------------------------------------------------------------------|
| `sgrade`   | Updates sgrade automatically, See [Update itself](https://github.com/LucasTavaresA/sgrade#update-itself)               |
| `packages` | Updates packages and your system using your distro package manager.                                                    |
| `etc`      | On arch based distros merge new versions of system files that come after updates, **depends on pacman-contrib**.       |
| `nodejs`   | Run `yarn global update` if it is installed, or `npm update -g` if `npm root -g` is a path inside your home directory. |
| `pip`      | Update all pip packages.                                                                                               |
| `dotnet`   | Update all global dotnet packages.                                                                                     |
| `fish`     | Update all fish plugins if `fisher` is installed.                                                                      |
| `rustup`   | Run `rustup update` and `rustup self-update`.                                                                          |
| `cargo`    | Update all cargo packages if `cargo-update` is installed.                                                              |
| `flatpak`  | Update all flatpaks.                                                                                                   |
| `snap`     | Update all snaps.                                                                                                      |
| `brew`     | Update all brew packages.                                                                                              |
| `nix`      | Update all nix packages.                                                                                               |
| `pearl`    | Run `pearl update`.                                                                                                    |
| `gem`      | Run `gem upgrade --user-install` if `~/.gem` exists.                                                                   |
| `gh`       | Update all gh extensions.                                                                                              |
| `custom`   | Run `~/.config/sgrade/custom`.                                                                                         |

## Update itself

Keeps and pulls a clone of sgrade in `$XDG_DATA_HOME/sgrade` or `$HOME/.local/share/sgrade`,
You can change that by changing `SG_PATH` to a different location

When the repo pulls a new version it asks to substitute the sgrade in your path


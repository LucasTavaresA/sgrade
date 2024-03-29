# sgrade

Simple alternative to [topgrade](https://github.com/topgrade-rs/topgrade)

or Suckless, Shellscript... maybe S tier

![screenshot](https://user-images.githubusercontent.com/80704612/209752444-2ec0ef56-8ddc-4d5f-80b9-d540727014e1.png)

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

| Resource    | Description                                                                                                                                               |
|:-----------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sgrade`    | Updates sgrade automatically, See [Update itself](https://github.com/LucasTavaresA/sgrade#update-itself)                                                  |
| `packages`  | Updates packages and your system using your distro package manager, See the [source code](https://github.com/LucasTavaresA/sgrade/blob/main/sgrade#L153). |
| `etc`       | Merge new etc files, See [Etc](https://github.com/LucasTavaresA/sgrade#etc).                                                                              |
| `nodejs`    | Run `yarn global update`, or `npm update -g` if `npm root -g` is a path inside your $HOME.                                                                |
| `pip`       | Update pip and pipx if they are inside $HOME, then upgrade all packages installed using [pipx](https://github.com/pypa/pipx).                             |
| `go`        | Update all go packages with [gup](https://github.com/nao1215/gup).                                                                                        |
| `dotnet`    | Update all global dotnet packages.                                                                                                                        |
| `fish`      | Update all fish plugins.                                                                                                                                  |
| `rustup`    | Run `rustup update` and `rustup self-update`.                                                                                                             |
| `cargo`     | Update all cargo packages using [cargo-update](https://github.com/nabijaczleweli/cargo-update).                                                           |
| `flatpak`   | Update all flatpaks.                                                                                                                                      |
| `snap`      | Update all snaps.                                                                                                                                         |
| `brew`      | Update all brew packages.                                                                                                                                 |
| `nix`       | Update all nix packages.                                                                                                                                  |
| `pearl`     | Run `pearl update`.                                                                                                                                       |
| `gem`       | Run `gem upgrade` or `gem upgrade --user-install` if `~/.gem` exists.                                                                                     |
| `gh`        | Update all gh extensions.                                                                                                                                 |
| `distrobox` | Update all distrobox containers.                                                                                                                          |
| `custom`    | Run `~/.config/sgrade/custom`.                                                                                                                            |

## Update itself

Depends on curl or wget

When a new version is downloaded it shows the difference in the new version
and asks to substitute the sgrade in your path

## Etc

Works only specific distros

- On **void linux** install `xtools`
- On **arch based distros** install `pacman-contrib`


# FEMM 4.2 Flatpak Unofficial

This is a flatpak version of [FEMM 4.2](https://www.femm.info) from David Meeker, Ph.D. 

My effort was only to pack essential packages to run wine and provide a script to download and install FEMM.

## Install

Flatpak is native for a majority of distributions. If this is not your case, you can [install flatpak](https://flatpak.org/setup/).

Download platpak and install:

```flatpak install --user info.femm.flatpak.flatpak```

First time it will adjust everything and download femm to install. It can take a while. You can run directly from your application menu, however it is better to keep track of the installation process. My suggestion is to run it from CLI.

    
```flatpak run info.femm.flatpak```

It will also copy mod mfiles to work with octave.

#### Known bugs

Flatpak may not install i386 runtime for you. If so, you can have a missing /app/bin/wine.

If so:

```flatpak install --user org.freedesktop.Platform.Compat.i386/x86_64/21.08```

I'm working on a repository...

## Octave

It just set everything automatcally. Just add the path

```addpath("~/.local/share/femm-flatpak/drive_c/femm42/mfiles/");```

## Python

Same as octave, just point to the correct folder.

```femm.openfemm(winepath='/home/<change_to_your_username>/.local/share/femm-flatpak/', femmpath='/home/<change_to_your_username>/.local/share/femm-flatpak/drive_c/femm42/bin/')```

## Building your own flatpak

```git clone https://github.com/thalesmaoa/femm-unofficial.git```

```cd femm-flatpak```

Install flatpak builder.

``` sudo apt install flatpak-builder```

Prepare for compiling wine. It's gonna take a while.

```flatpak-builder --force-clean femm-flatpak info.femm.flatpak.yml```

To test:

```flatpak-builder --run femm-flatpak info.femm.flatpak.yml femm.sh```

### Repository

Build local repository

```flatpak-builder --repo=thalesmaoa --force-clean femm-unofficial info.femm.flatpak.yml```

Install

```flatpak --user remote-add --no-gpg-verify thalesmaoa thalesmaoa```

List local packages repository

```flatpak remotes```

Install the package

```flatpak --user install thalesmaoa info.femm.flatpak```

Running the program

```flatpak run info.femm.flatpak```

### Single-file bundles

```flatpak build-bundle thalesmaoa info.femm.flatpak.flatpak info.femm.flatpak```

### Acknowledge

 - [fastrizwaan](https://github.com/fastrizwaan) for flatpak-wine.

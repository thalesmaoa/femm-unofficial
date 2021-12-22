# FEMM 4.2 Flatpak Unofficial

This is a flatpak version of [FEMM 4.2](https://www.femm.info) from David Meeker, Ph.D. 

My effort was only to pack essential packages to run wine and provide a script to download and install FEMM.

## Install

Flatpak is native for a majority of distributions. If this is not your case, you can [install flatpak](https://flatpak.org/setup/).

I'm working on a repository...

## Octave

It just set everything automatcally. Just add the path

```addpath("~/.local/share/femm-unofficial/drive_c/femm42/mfiles");```

## Python

Same as octave, just point to the correct folder.

```femm.openfemm(winepath='~/.local/share/wine-flatpak',femmpath='~/.local/share/femm-unofficial/drive_c/femm42')```

## Building your own flatpak

```git clone https://github.com/thalesmaoa/femm-unofficial.git```

```cd femm-unofficial```

Install flatpak builder.

``` sudo apt install flatpak-builder```

Prepare for compiling wine. It's gonna take a while.

```flatpak-builder --force-clean femm-unoficial info.femm.unofficial-manifest.yml```

To test:

```latpak-builder --run femm-unoficial info.femm.unofficial-manifest.yml```

### Acknowledge

 - [fastrizwaan](https://github.com/fastrizwaan) for flatpak-wine.

# FEMM 4.2 Flatpak Unofficial

This is a flatpak version of [FEMM 4.2](https://www.femm.info) from David Meeker, Ph.D. 

My effort was only to pack essential packages to run wine and provide a script to download and install FEMM.

## Octave

It just set everything automatcally. Just add the path

```addpath("~/.local/share/femm-unofficial/drive_c/femm42/mfiles");```

## Python

Same as octave, just point to the correct folder.

```femm.openfemm(winepath='~/.local/share/wine-flatpak',femmpath='~/.local/share/femm-unofficial/drive_c/femm42')```

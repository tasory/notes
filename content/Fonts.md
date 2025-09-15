*(info from archwiki and gentoo wiki)*
*by tasory*
# 0. Introduction
Fonts are stored in the following directories:
```
~/.fonts 
~/.local/share/fonts
/usr/local/share/fonts/
```

> [!Warning] 
> In the past **`~/.fonts`** was used, but is now deprecated.

> [!Warning] 
> **`/usr/share/fonts/`** is under the purview of the package manager, and should not be modified manually.

The creation of a sub-directory structure is up to the user, and varies among Linux distributions. For clarity, it is good to keep each font in its own directory.

The font files need to have sufficient read permissions for all users, i.e. at least chmod `444` for files, and `555` for directories.
# 1. Installing
## 1.1 installation via package manager

> [!Tip] 
> **Often, font packages have the suffix `font-` or `-ttf` in their names.**

Gentoo repository has category **`media-fonts`**, that contain fonts.
In the Arch Linux repository, font packages have the **`ttf-`** and **`otf-`** prefixes.
## 1.2 Installing manually
  
- For a single user, install fonts to `~/.local/share/fonts/`.
- For system-wide (all users) installation, place your fonts under `/usr/local/share/fonts/`.

After moving the fonts in the directory, update the **Fontconfig** cache:
```
$ fc-cache -fv
```

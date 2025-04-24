# Arch Mac Style Plymouth Theme

Plymouth theme that heavily inspired by MacOS boot animation with pre-installed Arch logo instead of Apple logo.

<!-- TODO: Add screenshot -->

## How to place your Logo

1. Replace the image "images/watermark.png"  by your own logo

The optional dimensions are:
square:           130px x 130px
rectangular:      244px x 130px

The sample images from the "samples"-folder can be used for comparison.
Everything below the black box should remain free. This space is used as a gap to the progress bar.
The black box (guide lines) can still remain in the picture as such.
The background of the Plymouth theme is black, so these "guide lines" are not visible.
But you can remove them if you wish. It's up to you to decide how you want it.

## Setup

1. Clone repo inside /usr/share/plymouth/themes/arch-mac-style
2. `git clone https://github.com/kakawait/arch-mac-style-plymouth-theme.git /usr/share/plymouth/themes/arch-mac-style`

Then depending your base linux os, please follow:

### Ubuntu/Linux Mint/Tuxedo OS

```bash
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/arch-mac-style/arch-mac-style.plymouth 110

# Select the Theme
sudo update-alternatives --config default.plymouth

# Rebuild the initial Ramdisk:
sudo update-initramfs -u -k all
```

### Debian/Arch Linux

```bash
# Please look, if the theme "arch-mac-style" is recognized
sudo plymouth-set-default-theme -l

# Apply the theme
sudo plymouth-set-default-theme -R arch-mac-style
```

### Fedora

```bash
# Please look, if the theme "arch-mac-style" is recognized
sudo plymouth-set-default-theme -l

# Apply the theme
sudo plymouth-set-default-theme -R arch-mac-style

# Rebuild the initrd

sudo dracut --regenerate-all -f
```

# Credits

Based on https://www.gnome-look.org/p/2112595

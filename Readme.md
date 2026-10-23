# Canon UFR II Printer Driver for Arch Linux

An Arch Linux PKGBUILD for Canon's proprietary UFR II printer driver, version 6.40.

## Package

- **Package:** `cnrdrvcups-ufr2-uk`
- **Version:** 6.40
- **Architecture:** x86_64
- **Source:** [Canon Linux UFR II Driver](https://gdlp01.c-wss.com/gds/8/0100007658/51/linux-UFRII-drv-v640-m17n-05.tar.gz)

## Installation

Clone the AUR package and build it using `makepkg`:

```bash
git clone https://aur.archlinux.org/cnrdrvcups-ufr2-uk.git
cd cnrdrvcups-ufr2-uk
makepkg -si
```

## Notes

- The driver is proprietary software distributed by Canon.
- The PKGBUILD downloads the driver archive from Canon and extracts the x86_64 RPM payload for packaging.
- This package provides printing-driver support; scanner functionality is not included or guaranteed.

## License

The PKGBUILD is community-maintained packaging work. Canon's driver remains subject to Canon's applicable license terms.

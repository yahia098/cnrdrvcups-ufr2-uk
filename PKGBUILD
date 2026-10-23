
pkgname=cnrdrvcups-ufr2-uk
pkgver=6.40
pkgrel=2
pkgdesc="Canon UFR II Printer Driver for Linux"
arch=('x86_64')
license=('custom')
depends=('cups' 'gtk3' 'jbigkit' 'libgcrypt' 'libjpeg-turbo')
makedepends=('rpm-tools' 'cpio')
options=('!strip')

source=("https://gdlp01.c-wss.com/gds/8/0100007658/51/linux-UFRII-drv-v640-m17n-05.tar.gz")
sha256sums=('SKIP')

prepare() {
    local archive="$srcdir/linux-UFRII-drv-v640-m17n-05.tar.gz"
    local rpm_file="$srcdir/extracted/linux-UFRII-drv-v640-m17n/x64/RPM/cnrdrvcups-ufr2-uk-6.40-1.05.x86_64.rpm"

    mkdir -p "$srcdir/extracted" "$srcdir/package"

    tar -xf "$archive" -C "$srcdir/extracted"

    if [[ ! -f "$rpm_file" ]]; then
        error "Expected Canon RPM not found: $rpm_file"
    fi

    cd "$srcdir/package"
    rpm2cpio "$rpm_file" | cpio -idm --quiet

    if [[ -d usr/lib64 ]]; then
        mkdir -p usr/lib
        cp -a usr/lib64/. usr/lib/
        rm -rf usr/lib64
    fi
}

package() {
    cp -a "$srcdir/package/." "$pkgdir/"
}


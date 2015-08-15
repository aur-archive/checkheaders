# Maintainer: Mariusz Libera <mariusz.libera@gmail.com>
pkgname=checkheaders
pkgver=1.0.1
pkgrel=3
pkgdesc="Detect unnecessary includes in C/C++ programs"
arch=('i686' 'x86_64')
url="http://code.google.com/p/checkheaders/"
license=('GPL3')
depends=('gcc-libs')
changelog=Changelog
source=("http://checkheaders.googlecode.com/files/${pkgname}-${pkgver}.zip")
sha256sums=('6e4e81e160324ff9990520fe89ea0f2139e7f5c95674014ce35b496cb4d357e0')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    make -e
}

package() {
    cd "$srcdir/$pkgname-$pkgver"

    # executable
    install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname"

    # documentation
    install -Dm644 readme.txt "$pkgdir/usr/share/doc/$pkgname/readme.txt"
}


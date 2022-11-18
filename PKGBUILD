# $Id$

pkgname=glacier-calendar
pkgver=0.0.3
pkgrel=1
pkgdesc="Nemo calendar"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-calendar"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app>=0.9'
	'nemo-qml-plugin-calendar')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('b441c1a0a44f848c2f6fba09a00a4ae39bda878f36ab6a5d3ec9b640d3286cfa')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}

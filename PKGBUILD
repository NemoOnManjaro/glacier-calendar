# $Id$

pkgname=glacier-calendar
pkgver=0.0.2
pkgrel=1
pkgdesc="Nemo calendar"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-calendar"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'nemo-qml-plugin-calendar')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('9acdc7245100655c8250d56f0fa97159c9f268e216b2c0a1a636f57453b5c2d2')

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

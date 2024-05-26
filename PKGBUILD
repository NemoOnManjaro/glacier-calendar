# $Id$

pkgname=glacier-calendar
pkgver=0.1
pkgrel=2
pkgdesc="Nemo calendar"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-calendar"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app>=0.9'
	'nemo-qml-plugin-calendar>=0.7.4')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('fae1bd7f7715dafb17deaec6c9ef6718d4cdebdf2d231a01819c70fcba699dc7')

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

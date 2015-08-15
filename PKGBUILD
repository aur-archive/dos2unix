# Maintainer: Renato Garcia <fgar.renatoATgmailDOTcom>
# Contributor: Gerson E. Ruotolo <gersonruotolo@globo.com>

pkgname=dos2unix
pkgver=5.3.1
pkgrel=3
pkgdesc='Text file format converter'
arch=('i686' 'x86_64')
url='http://waterlan.home.xs4all.nl/dos2unix.html'
license=('BSD')
depends=('glibc')
makedepends=('perl')
conflicts=('hd2u')
source=("http://waterlan.home.xs4all.nl/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('438c48ebd6891b80b58de14c022ca69e')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  install -D -m644 COPYING.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

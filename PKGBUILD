# Maintainer: Gerardo Exequiel Pozzi <vmlinuz386@yahoo.com.ar>

pkgname=libcap-ng
pkgver=0.6.6
pkgrel=1
pkgdesc="A library intended to make programming with POSIX capabilities much easier than the traditional libcap"
arch=('i686' 'x86_64')
url="http://people.redhat.com/sgrubb/libcap-ng/"
license=('GPL2' 'LGPL2.1')
depends=('glibc')
options=('!libtool')
changelog='ChangeLog'
source=(http://people.redhat.com/sgrubb/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('eb71f967cecb44b4342baac98ef8cb0f')

build() {
  cd $srcdir/$pkgname-$pkgver

  ./configure --prefix=/usr --enable-static=no
  make
}

package() {
  cd $srcdir/$pkgname-$pkgver

  make DESTDIR=$pkgdir install
}

# vim:set ts=2 sw=2 et:

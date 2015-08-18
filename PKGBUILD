#Maintainer: Joao Cordeiro <jlcordeiro at gmail dot com>
#Contributor: Tetsuharu <tetsuharu@gmail.com>
pkgname=xfrisk
pkgver=1.2
pkgrel=4
pkgdesc="Old-school fully networkable Risk clone written for Xaw."
arch=('i686' 'x86_64')
license=('GPL-2')
url="http://tuxick.net/xfrisk/"
depends=('glibc' 'libxaw')
source=('https://launchpad.net/ubuntu/intrepid/+source/xfrisk/1.2-3/+files/xfrisk_1.2.orig.tar.gz')
md5sums=('857ce8a2522eb6ee1321da8a9e705cf0')

build() {
  mkdir -p $pkgdir/usr/{local/lib/xfrisk,bin}

  cd $srcdir/$pkgname-$pkgver

  sed -i 's|helvetica|fixed|' *

  make

  install -D -m 755 {aiColson,aiConway,aiDummy,friskserver,risk,xfrisk} $pkgdir/usr/bin/ ;
  install -D -m 644 {Aide,Countries,Help,World}.risk $pkgdir/usr/local/lib/xfrisk/
}

# vim:set ts=2 sw=2 et:

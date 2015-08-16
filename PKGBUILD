# Contributor: dorphell <dorphell@archlinux.org>
# Contributor: Tom Newsom <Jeepster@gmx.co.uk>

pkgname=netselect
pkgver=0.3
pkgrel=2
pkgdesc="An ultrafast intelligent parallelizing binary-search implementation of ping"
arch=(i686 x86_64)
url="http://alumnit.ca/~apenwarr/netselect/index.html"
license=(custom)
depends=()
source=(http://apenwarr.ca/netselect/$pkgname-$pkgver.tar.gz
        license.txt)
md5sums=('3a3714946db2458e5db3d55373057ef2'
         '741ea171051c5cbac5ff18326c11d65e')

build() {
  cd $srcdir/$pkgname

  sed -i '/sudo /d' Makefile

  make
}

package() {

  install -D -m4755 $srcdir/$pkgname/netselect $pkgdir/usr/bin/netselect
  install -D -m644  $srcdir/license.txt \
    $pkgdir/usr/share/licenses/netselect/LICENSE
}

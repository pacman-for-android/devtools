# Maintainer: Jason Chu <jason@archlinux.org>

pkgname=devtools
pkgver=0.6.3
pkgrel=1
pkgdesc="A few tools to help Arch Linux developers"
arch=(i686 x86_64)
license=('GPL')
url="http://projects.archlinux.org/git/?p=devtools.git"
depends=(namcap)
source=(ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('3f3b116a06372fda54bd2c4f7bf993c6')

build() {
  cd $startdir/src/$pkgname-$pkgver
  make DESTDIR=$startdir/pkg install
}

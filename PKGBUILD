# Maintainer: Jason Chu <jason@archlinux.org>

pkgname=devtools
pkgver=0.6.4
pkgrel=1
pkgdesc="A few tools to help Arch Linux developers"
arch=(i686 x86_64)
license=('GPL')
url="http://projects.archlinux.org/git/?p=devtools.git"
depends=(namcap)
source=(ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('71bc2abe78acf3e496b1f42fa4fb3d9e')

build() {
  cd $startdir/src/$pkgname-$pkgver
  make DESTDIR=$startdir/pkg install
}

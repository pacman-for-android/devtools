# Maintainer: Jason Chu <jason@archlinux.org>

pkgname=devtools
pkgver=0.7.0
pkgrel=1
pkgdesc="A few tools to help Arch Linux developers"
arch=('any')
license=('GPL')
url="http://projects.archlinux.org/git/?p=devtools.git"
depends=('namcap')
conflicts=('aurtools')
source=(ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('d098ac71248a7a30b3bc700b1087bc78')

build() {
  cd $srcdir/$pkgname-$pkgver
  make DESTDIR=$pkgdir install
}

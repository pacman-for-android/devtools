# Maintainer: Jason Chu <jason@archlinux.org>

pkgname=devtools
pkgver=0.8.0
pkgrel=1
pkgdesc="A few tools to help Arch Linux developers"
arch=('any')
license=('GPL')
url="http://projects.archlinux.org/?p=devtools.git"
depends=('namcap')
conflicts=('aurtools')
source=(ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('03749475e668d90eb684db543027efd0')

build() {
  cd $srcdir/$pkgname-$pkgver
  make DESTDIR=$pkgdir install
}

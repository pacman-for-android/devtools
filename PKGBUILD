# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20151002
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync' 'arch-install-scripts')
source=("https://sources.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig})
validpgpkeys=('487EACC08557AD082088DABA1EB2638FF56C0C53'
              '4AA4767BBC9C4B1D18AE28B77F2D434B9741E8AC'
              '86CFFCA918CF3AF47147588051E8B148A9999C34')
md5sums=('a8d1234c6c7b936a850858e3bc03b2c8'
         'SKIP')

build() {
	cd "${pkgname}-${pkgver}"
	make PREFIX=/usr
}

package() {
	cd "${pkgname}-${pkgver}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

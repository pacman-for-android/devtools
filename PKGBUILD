# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=0.9.3
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('9877c382071eda5ce01c18634fb9b8c9')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make DESTDIR=${pkgdir} install
}

# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=0.9.4
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('778a53928b4bbe94b98f252cc2df5d67')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make DESTDIR=${pkgdir} install
}

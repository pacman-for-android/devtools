# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20111220
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz"
        "ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz.sig")
md5sums=('2ee85a079f2cfbb851b1d75d0d3f4d86'
         'c0c35c6a202df277f25a61f9ffac9c1d')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

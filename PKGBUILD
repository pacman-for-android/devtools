# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20121003
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync' 'arch-install-scripts')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz"
        "ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz.sig")
md5sums=('7a20ec4fe7239a693c2d3430dee99344'
         '0b20722bbeba43d9e907b61b02359c51')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20120611
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz"
        "ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz.sig")
md5sums=('49a8b1c256790063edc3cd54249e0e21'
         '444ad039068dbd9279d0950e2ec9115f')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

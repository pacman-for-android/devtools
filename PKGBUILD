# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20120720
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz"
        "ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz.sig")
md5sums=('d1ba08ff9610584e5fa3a6bdc8506865'
         '248dc8c61adf74ce26883979a11adbe9')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

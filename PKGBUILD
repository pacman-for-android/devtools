# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=0.9.24
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('85b8e4291b3a06899139af07806fbb62')

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=0.9.23
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync')
source=("ftp://ftp.archlinux.org/other/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('7f7e43464b50942ac3655aaad5167f34')

package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make DESTDIR=${pkgdir} install
}

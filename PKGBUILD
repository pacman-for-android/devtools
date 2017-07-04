# Maintainer: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
pkgver=20170320
pkgrel=3
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='http://projects.archlinux.org/devtools.git/'
depends=('namcap' 'openssh' 'subversion' 'rsync' 'arch-install-scripts')
source=("https://sources.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig}
        '0001-makechrootpkg-Delete-chroot-subvols-recursively-when.patch'
        '0002-Sync-makepkg.conf-files-with-pacman-5.0.2-2.patch')
validpgpkeys=('487EACC08557AD082088DABA1EB2638FF56C0C53'
              '4AA4767BBC9C4B1D18AE28B77F2D434B9741E8AC'
              '86CFFCA918CF3AF47147588051E8B148A9999C34'
              '8FC15A064950A99DD1BD14DD39E4B877E62EB915'
              '8218F88849AAC522E94CF470A5E9288C4FA415FA')
md5sums=('e401f4e3d1074b80060390b9812766f1'
         'SKIP'
         '678ec14b148dbe88cbac92a1cefa57d5'
         'a5b4e14d9870cfcf0f841b438ee0d8cc')

prepare() {
	cd "${pkgname}-${pkgver}"
	patch -Np1 -i ../0001-makechrootpkg-Delete-chroot-subvols-recursively-when.patch
	patch -Np1 -i ../0002-Sync-makepkg.conf-files-with-pacman-5.0.2-2.patch
}

build() {
	cd "${pkgname}-${pkgver}"
	make PREFIX=/usr
}

package() {
	cd "${pkgname}-${pkgver}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

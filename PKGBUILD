# Maintainer: Levente Polyak <anthraxx[at]archlinux[dot]org>
# Contributor: Pierre Schmitz <pierre@archlinux.de>

pkgname=devtools
epoch=1
pkgver=1.0.0
pkgrel=1
pkgdesc='Tools for Arch Linux package maintainers'
arch=('any')
license=('GPL')
url='https://gitlab.archlinux.org/archlinux/devtools'
depends=(
  arch-install-scripts
  awk
  bash
  binutils
  coreutils
  diffutils
  findutils
  grep
  jq
  openssh
  parallel
  rsync
  sed
  util-linux

  bzr
  git
  mercurial
  subversion
)
makedepends=(
  asciidoc
  shellcheck
)
optdepends=('btrfs-progs: btrfs support')
replaces=(devtools-git-poc)
source=(https://gitlab.archlinux.org/archlinux/devtools/-/releases/${pkgver}/downloads/devtools-${pkgver}.tar.gz{,.sig})
validpgpkeys=(
  '4AA4767BBC9C4B1D18AE28B77F2D434B9741E8AC' # Pierre Schmitz <pierre@archlinux.org>
  '86CFFCA918CF3AF47147588051E8B148A9999C34' # Evangelos Foutras <foutrelis@archlinux.org>
  '8FC15A064950A99DD1BD14DD39E4B877E62EB915' # Sven-Hendrik Haase <svenstaro@archlinux.org>
  'A2FF3A36AAA56654109064AB19802F8B0D70FC30' # Jan Alexander Steffens (heftig) <heftig@archlinux.org>
  'B81B051F2D7FC867AAFF35A58DBD63B82072D77A' # Sébastien Luttringer <seblu@archlinux.org>
  '6645B0A8C7005E78DB1D7864F99FFE0FEAE999BD' # Allan McRae (Developer) <allan@archlinux.org>
  'E240B57E2C4630BA768E2F26FC1B547C8D8172C8' # Levente Polyak <anthraxx@archlinux.org>
)
sha256sums=('96bb61e5a59ae9c3a2efe05a6925159b50007b96cc798386223691454dd36aed'
            'SKIP')
b2sums=('055f9514cd2304b7299d14a9e1c760b7ef173a93a77725fab260d488835c95a2f154e5c3edb6896505a6039f4a429f2ec84981292a36b9b8cbf35b79c07c469a'
        'SKIP')

build() {
  cd ${pkgname}-${pkgver}
  make BUILDTOOLVER="${epoch}:${pkgver}-${pkgrel}-${arch}" PREFIX=/usr
}

package() {
  cd ${pkgname}-${pkgver}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
}

# vim: ts=2 sw=2 et:

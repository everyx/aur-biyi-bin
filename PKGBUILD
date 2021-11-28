# Maintainer: everyx <lunt.luo at gmail dot com>

pkgname=biyi-bin
_pkgname=${pkgname%-bin}
_reponame=${_pkgname}_app
pkgver=0.3.4
_buildnumber=7
pkgrel=1
pkgdesc="Biyi (比译) is a convenient translation and dictionary app written in dart / Flutter. "
arch=('x86_64')
url="https://biyidev.com/"
license=('AGPL3')
depends=('libkeybinder3' 'libappindicator-gtk3')
provides=("${_pkgname}")
conflicts=("${_pkgname}")
# options=('!strip')
source_x86_64=("https://github.com/biyidev/${_reponame}/releases/download/v${pkgver}/biyi-${pkgver}+${_buildnumber}-linux.deb")
sha256sums_x86_64=('4d135da97c68a19cd18761b2217c0e8e169625ba5dd01ef7c1f60b01d2f708c2')

prepare() {
    bsdtar -xpf "data.tar.xz"
}

package() {
  cp -r "${srcdir}/usr" "${pkgdir}"
  chmod -R 755 "${pkgdir}/usr"
}
# vim: set sw=2 ts=2 et:

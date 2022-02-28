# Maintainer: alexandriaptt alxpettit@gmail.com
# Contributor: thegala <thegala at disroot dot org>
pkgname=icestudio-appimage
pkgver=0.9.0
pkgrel=1
pkgdesc="A real gamechanger in the world of Open Source FPGAs"
arch=('x86_64')
url='https://icestudio.io/'
license=('GPL2')
depends=('python' 'gconf')
makedep=('fakeroot')
provides=("icestudio")
conflicts=('icestudio')
source=("https://github.com/FPGAwars/icestudio/releases/download/v${pkgver}/icestudio-${pkgver}-linux64.AppImage"
        "icestudio.sh" "icestudio.desktop" "icestudio-logo.png")
sha512sums=('a9e3bf171ba70643f5bf6075405bf4a41173704c58c5ededba00f4010d253293b766e968576366a7c88fd7addf84a25710eabd18c2fd45e3d5244664ac7d4ecc'
            '03027bf85087ec373b651554a5edc564204199a43fae36475e0db0946f0b83d8fd342fada4f58d5fd749c5c81794d8fe64a006e703a99e5a061fe11bf234b2b1'
            '05dd179d8dcb40ca6d91e5549da8fa2e4d661d9b68ec235bc6db0fa40f575dcb9863c9b0bfa6927d0e874a3476f5f5b1e6cbfb324fe49df3c8897c5dfe3a9965'
            '25395f85365313ac72fc1524d50b6d7bd4d1477337fdead48038c88d86ec5272d7fd3cb292313089146e2ac60210a7711f3c110f2c981899cf9f76e470acc070')
options=(!strip)
_filename=./icestudio-${pkgver}-linux64.AppImage

# prepare() {
#   cd "${srcdir}"
#   chmod +x ${_filename}
#   ${_filename} --appimage-extract > /dev/null 2>&1 &
# }

package() {
  install -Dm755 "${srcdir}/${_filename}" "${pkgdir}/opt/appimages/icestudio.AppImage"
  install -Dm755 "${srcdir}/icestudio.sh" "${pkgdir}/usr/bin/icestudio"

  install -Dm644 "${srcdir}/icestudio.desktop" "${pkgdir}/usr/share/applications/icestudio.desktop"
  install -Dm644 "${srcdir}/icestudio-logo.png" "${pkgdir}/usr/share/icons/hicolor/256x256/apps/icestudio.png"
}

# vim:set ts=2 sw=2 et:

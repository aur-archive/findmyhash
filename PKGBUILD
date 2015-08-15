# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Mauro Andreolini <mauro.andreolini@unimore.it>
pkgname=findmyhash
pkgver=1.1.2
pkgrel=3
epoch=
pkgdesc="Crack different types of hashes using free online services"
arch=('any')
url="http://code.google.com/p/findmyhash/"
license=('GPL3')
depends=(python2 python2-httplib2)
install=
changelog=
source=("http://findmyhash.googlecode.com/files/${pkgname}_v${pkgver}.py")
md5sums=('4c4eaa71a74c5965ee7f8742025bb776')

build() {
  cd "${srcdir}/"
  (echo "#!/usr/bin/env python2"; cat ${pkgname}_v${pkgver}.py) > tmp
  mv tmp ${pkgname}_v${pkgver}.py
}

package() {

  cd ${srcdir}
  install -D -m 755 ${pkgname}_v${pkgver}.py ${pkgdir}/usr/bin/${pkgname}
}

# vim:set ts=2 sw=2 et:

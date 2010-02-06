# $Id: PKGBUILD 563 2009-08-03 18:43:58Z jlichtblau $
# Maintainer: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Jaroslav Lichtblau <dragonlord@aur.archlinux.org>
# Contributor: Angel 'angvp' Velasquez <angvp[at]archlinux.com.ve>
# Contributor: William Rea <sillywilly@gmail.com>
# Contributor: Guillem Rieu <guillemr@gmx.net>

pkgname=python-lxml
pkgver=2.2.4
pkgrel=2
pkgdesc="Python binding for the libxml2 and libxslt libraries"
arch=('i686' 'x86_64')
license=('BSD' 'GPL' 'custom')
url="http://codespeak.net/lxml"
depends=('python' 'libxslt')
optdepends=("beautiful-soup: support for parsing not well formed HTML")
conflicts=('lxml')
replaces=('lxml')
source=(http://codespeak.net/lxml/lxml-$pkgver.tgz)
md5sums=('077841e74ee728e7746b65d8483274be')

build() {
  cd ${srcdir}/lxml-$pkgver

  python setup.py install --root=${pkgdir} || return 1

  install -D -m644 LICENSES.txt ${pkgdir}/usr/share/licenses/$pkgname/LICENSE || return 1
  install -D -m644 doc/licenses/BSD.txt ${pkgdir}/usr/share/licenses/$pkgname/BSD.txt || return 1
  install -D -m644 doc/licenses/elementtree.txt ${pkgdir}/usr/share/licenses/$pkgname/elementtree.txt || return 1
}

# $Id$
# Maintainer: Jaroslav Lichtblau <dragonlord@aur.archlinux.org>
# Contributor: Angel 'angvp' Velasquez <angvp[at]archlinux.com.ve>
# Contributor: William Rea <sillywilly@gmail.com>
# Contributor: Guillem Rieu <guillemr@gmx.net>

pkgname=python-lxml
pkgver=2.2.2
pkgrel=1
pkgdesc="Python binding for the libxml2 and libxslt libraries"
arch=('i686' 'x86_64')
license=('BSD' 'GPL' 'custom')
url="http://codespeak.net/lxml"
depends=('python' 'libxslt')
source=(http://codespeak.net/lxml/lxml-$pkgver.tgz)
conflicts=('lxml')
replaces=('lxml')

md5sums=('2f2fcb6aae51b5b417a3c0a6b256ec56')

build() {
  cd ${srcdir}/lxml-$pkgver

  python setup.py install --root=${pkgdir} || return 1

  install -D -m644 LICENSES.txt ${pkgdir}/usr/share/licenses/$pkgname/LICENSES.txt || return 1
  install -D -m644 doc/licenses/BSD.txt ${pkgdir}/usr/share/licenses/$pkgname/BSD.txt || return 1
  install -D -m644 doc/licenses/elementtree.txt ${pkgdir}/usr/share/licenses/$pkgname/elementtree.txt || return 1
}

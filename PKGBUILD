# Maintainer: Jeremy Deininger <jeremydeininger@gmail.com>

pkgname=bbs-keyring
pkgver=20160508
pkgrel=1
pkgdesc='Blackbird PGP keyring'
arch=('any')
url='https://github.com/bbcx/bbs-keyring.git'
makedepends=('git')
license=('GPL')
install="${pkgname}.install"
source=("bbs-keyring::git://github.com/bbcx/bbs-keyring.git")
md5sums=('SKIP')

pkgver() {
	cd "$srcdir"/bbs-keyring
	git log -1 --format="%cd" --date=short | sed 's|-||g'
}

package() {
	cd "$srcdir"/bbs-keyring
	make PREFIX=/usr DESTDIR=${pkgdir} install
}

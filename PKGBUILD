# Maintainer: Magnus Anderson <magnus@iastate.edu>
pkgname=pacman-noob-tutorial
pkgver=1
pkgrel=1
pkgdesc="Symlinks other distributions' package managers to a tutorial about pacman to improve new user experience"
arch=('any')
license=('Unlicense')
url="https://www.youtube.com/watch?v=3E8IGy6I9Wo"
depends=('less')
optdepends=('')
conflicts=

package() {
	mkdir -p "$pkgdir/usr/bin/"
	install -D -m755 ../pacman-help "${pkgdir}/usr/bin/pacman-help"
	# pacman-noob-tutorial should probably not be in $PATH
	mkdir -p "$pkgdir/usr/lib/"
	install -D -m755 ../pacman-noob-tutorial "${pkgdir}/usr/lib/$pkgname"
	# Create the symlinks
	ln -s /usr/lib/$pkgname "$pkgdir/usr/bin/apt"
	ln -s /usr/lib/$pkgname "$pkgdir/usr/bin/apt-get"
}

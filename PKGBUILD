# Maintainer: spikeyamk <vojtkoj@protonmail.com>
pkgname=st-spikeyamk
pkgver=0.8.4
pkgrel=1
pkgdesc="spikeyamk's 80's build of suckless st"
arch=(x86_64)
url="https://www.github.com/spikeyamk/st-spikeyamk.git"
license=('MIT')
groups=()
depends=('libxft' 'lib32-libxft' 'ttf-joypixels' 'ttf-hack')
makedepends=('git' 'make' 'harfbuzz' 'freetype2' 'libxext' 'ncurses')
checkdepends=()
optdepends=()
provides=(st-spikeyamk)
conflicts=(st)
replaces=()
backup=()
options=()
md5sums=('SKIP')
source=("git+$url")
noextract=()
validpgpkeys=()

build() {
	cd "$pkgname"
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
	cd "$pkgname"
	make PREFIX=/usr DESTDIR="$pkgdir/" install
}

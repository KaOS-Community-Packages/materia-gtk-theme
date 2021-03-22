pkgname=materia-theme
pkgver=20210322
pkgrel=2
pkgdesc="Materia theme for GTK"
arch=('any')
url="https://github.com/nana-4/materia-theme"
license=('GPL2')
depends=('gtk3' 'gtk-engine-murrine')
makedepends=('git' 'sassc' 'meson')
options=(!strip)
source=("https://github.com/nana-4/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('d822cfab25b0d3c6a750b09e14d7aa18')

package() {
	cd ${srcdir}/$pkgname-$pkgver
	meson "build" \
		-Dprefix="${pkgdir}/usr"
	ninja -C "build" install
}


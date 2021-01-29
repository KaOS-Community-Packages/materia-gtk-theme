pkgname=materia-gtk-theme
pkgver=20200916
pkgrel=1
pkgdesc="Materia theme for GTK"
arch=('any')
url="https://github.com/nana-4/materia-theme"
license=('GPL2')
depends=('gtk3' 'gtk-engine-murrine')
makedepends=('git' 'sassc' 'meson')
options=(!strip)
source=("https://github.com/nana-4/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('c9c9f2851c9677879801a7e04b8d3643')

package() {
	cd ${srcdir}/$pkgname-$pkgver
	meson "build" \
		-Dprefix="${pkgdir}/usr" \
		-Dgnome_shell_version=3.24
	ninja -C "build" install
}


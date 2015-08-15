pkgname=gmpc-awn
pkgver=11.8.16
pkgrel=2
pkgdesc="Integrates GMPC with Avant Window Navigator."
arch=('i686' 'x86_64')
url="http://gmpc.wikia.com/wiki/GMPC_PLUGIN_AWN"
license=('GPL')
depends=('avant-window-navigator' 'dbus-glib' 'gmpc>=11.8.16')
makedepends=('intltool')
options=('!libtool')
source=(http://download.sarine.nl/Programs/gmpc/$pkgver/$pkgname-$pkgver.tar.gz)
sha1sums=('0e36b50ea200d57a1b200fc0408714da78b77c93')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:

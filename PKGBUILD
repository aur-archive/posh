pkgname="posh"
#pkgver() {
    #pkgver=`head -n 1 $srcdir/debian/changelog | sed 's/.*(\([^]]*\)).*/\1/'`
#}
pkgver=0.12.4
pkgrel=1
pkgdesc="A strictly POSIX.2 compliant shell, with minimal extensions. Based on ksh."
#arch=(any)
arch=('i686' 'x86_64')
url="https://packages.debian.org/unstable/posh "
license=("GPLv2")
source=("http://ftp.de.debian.org/debian/pool/main/p/posh/posh_0.12.4.tar.xz")
md5sums=('36b612c80a6c46078302758ab797bfad')

prepare() {
	cd "$srcdir/$pkgname-$pkgver"
}

build() {
	cd "$srcdir/$pkgname-$pkgver"
    ./configure --prefix=/usr
    make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}

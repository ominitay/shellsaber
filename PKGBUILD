pkgname=shellsaber
pkgver=0.2.6
pkgrel=1
epoch=
pkgdesc="A mod manager written in POSIX-compliant shell script to support Beat Saber modding on Linux."
arch=('any')
url="https://github.com/ominitay/shellsaber"
license=('GPL3')
depends=('sh' 'jq' 'curl' 'wget' 'unzip')
checkdepends=(shellcheck)
backup=('etc/shaber/config')
source=("$pkgname-$pkgver.tar.gz::https://github.com/ominitay/$pkgname/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('c1639b841854b38654fb0391454f293c15a7787c0854c6cbd166dc8db075aee5')


check() {
  cd "$pkgname-$pkgver"

  shellcheck -x shaber
}

package() {
  cd "$pkgname-$pkgver"

  install -D -m 775 shaber "$pkgdir/usr/bin/shaber"
  install -D -m 664 config "$pkgdir/etc/shaber/config"
}

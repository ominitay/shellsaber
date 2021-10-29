pkgname=shellsaber
pkgver=0.3.1
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
sha256sums=('1baf1639be0833ee389196396d912426c0d8bef591d55ebe490aed1de906962e')


check() {
  cd "$pkgname-$pkgver"

  shellcheck -x shaber
}

package() {
  cd "$pkgname-$pkgver"

  install -D -m 775 shaber "$pkgdir/usr/bin/shaber"
  install -D -m 664 config.default "$pkgdir/etc/shaber/config"
}

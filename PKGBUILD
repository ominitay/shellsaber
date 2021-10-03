pkgname=shellsaber
pkgver=0.3.0
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
sha256sums=('e20ef29ac5646a08ee22f0e25390e478d78612c181f4c5e7f45cf84e94aa12fc')


check() {
  cd "$pkgname-$pkgver"

  shellcheck -x shaber
}

package() {
  cd "$pkgname-$pkgver"

  install -D -m 775 shaber "$pkgdir/usr/bin/shaber"
  install -D -m 664 config "$pkgdir/etc/shaber/config"
}

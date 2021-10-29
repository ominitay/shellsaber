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
sha256sums=('067604d48699681f996fb95857dc07a4eab11f20f5a23a2499cc6f822af7ff8b')


check() {
  cd "$pkgname-$pkgver"

  shellcheck -x shaber
}

package() {
  cd "$pkgname-$pkgver"

  install -D -m 775 shaber "$pkgdir/usr/bin/shaber"
  install -D -m 664 config.default "$pkgdir/etc/shaber/config"
}

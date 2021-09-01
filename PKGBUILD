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
sha256sums=('991b55a9d277b1a3e81bb8a5d48e0b99346047d74cdb000132c6062a3f7d18fc')


check() {
  cd "$pkgname-$pkgver"

  shellcheck -x shaber
}

package() {
  cd "$pkgname-$pkgver"

  install -D -m 775 shaber "$pkgdir/usr/bin/shaber"
  install -D -m 664 config "$pkgdir/etc/shaber/config"
}

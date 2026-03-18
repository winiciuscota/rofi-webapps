# Maintainer: Winícius Cota <winicius.cota@gmail.com>
pkgname=rofi-webapps
pkgver=1.0.0
pkgrel=1
pkgdesc="Rofi-based interface for managing web applications with icon search and CRUD operations"
arch=('any')
url="https://github.com/winiciuscota/rofi-webapps"
license=('MIT')
depends=('python' 'rofi' 'libnotify')
makedepends=('git')
source=("rofi-webapps-src::git+https://github.com/winiciuscota/rofi-webapps.git#tag=v${pkgver}")
sha256sums=('SKIP')

build() {
    : # pure python — nothing to compile
}

package() {
    cd "$srcdir/rofi-webapps-src"

    install -Dm755 rofi-webapps  "$pkgdir/usr/bin/rofi-webapps"
    install -Dm755 webapps-backend "$pkgdir/usr/lib/rofi-webapps/webapps-backend"

    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
    install -Dm644 LICENSE   "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

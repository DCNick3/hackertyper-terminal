# Maintainer: Jonas Tranberg <jonastranberg93@gmail.com>
pkgname=hackertyper-terminal
pkgver=r5.f1712e9
pkgrel=1
pkgdesc="A clone of the Hacker-Typer for the terminal"

arch=('any')
url="https://github.com/naueramant/hackertyper-terminal"
license=('MIT')
makedepends=('git')
source=('git+https://github.com/naueramant/hackertyper-terminal.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/hackertyper-terminal/"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -dm755 "$pkgdir/opt/hackertyper-terminal/"
  cp -r "$srcdir/hackertyper-terminal/" "$pkgdir/opt/"
}
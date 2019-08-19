pkgname=hackertyper-terminal
pkgver=r7.4b172fa
pkgrel=1
pkgdesc="A clone of the Hacker-Typer for the terminal"

arch=('any')
url="https://github.com/naueramant/hackertyper-terminal"
license=('MIT')
makedepends=('git')
source=('git+https://github.com/hackertyper-terminal.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/hackertyper-terminal/"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -dm755 "$pkgdir/usr/share/hackertyper-terminal"
  mkdir -p "$pkgdir/usr/share/hackertyper-terminal/" "$pkgdir/usr/bin"
  cp -r "$srcdir/hackertyper-terminal/kernel.txt" "$srcdir/hackertyper-terminal/hackertyper.sh" "$pkgdir/usr/share/hackertyper-terminal/"
  ln -s "/usr/share/hackertyper-terminal/hackertyper.sh" "$pkgdir/usr/bin/hackertyper"
}

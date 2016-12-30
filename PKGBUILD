# Maintainer: Jonas Tranberg <jonastranberg93@gmail.com>
pkgname=hackertyper-terminal-git
pkgver=r21.cd5d4aa
pkgrel=1
pkgdesc="A clone of the Hacker-Typer for the terminal"

arch=('any')
url="https://github.com/naueramant/hackertyper-terminal"
license=('MIT')
makedepends=('git')
source=('git+https://github.com/naueramant/hackertyper-terminal.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/hackertyper-terminal-git/"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -dm755 "$pkgdir/bin/share/hackertyper-terminal-git"
  cp -r "$srcdir/hackertyper-terminal-git/*" "$pkgdir/usr/share/hackertyper-terminal-git/"
  ln -s "/bin/hackertyper" "$pkgdir/usr/share/hackertyper-terminal-git/"
}
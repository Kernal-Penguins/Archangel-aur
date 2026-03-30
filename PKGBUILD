pkgname=archangel-cli
pkgver=0.1.3
pkgrel=1
pkgdesc="AI-driven CLI assistant for Arch-based Linux systems"
arch=('any')
url="https://github.com/Kernal-Penguins/ArchAngel---An-AI-driven-CLI-Assistant-for-arch-based-sytems"
license=('MIT')

install=archangel-cli.install

depends=(
'python'
'python-pipx'
)

optdepends=(
'ollama: AI features'
'jre-openjdk: backend service'
)

source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('a4ff3a5b823e83ffd4d341dc72634102e0a9235ff5b88004dc63f6dc981e607c')

package() {
cd "$srcdir/ArchAngel---An-AI-driven-CLI-Assistant-for-arch-based-sytems-$pkgver"

export PIPX_HOME="$pkgdir/opt/archangel"
export PIPX_BIN_DIR="$pkgdir/usr/bin"

pipx install . --force
}

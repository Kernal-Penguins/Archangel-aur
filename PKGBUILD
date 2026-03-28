pkgname=archangel-cli
pkgver=0.1.1
pkgrel=1
pkgdesc="AI-driven CLI assistant for Arch-based Linux systems"
arch=('x86_64')
url="https://github.com/Kernal-Penguins/ArchAngel---An-AI-driven-CLI-Assistant-for-arch-based-sytems"
license=('MIT')

depends=(
  'python'
  'python-typer'
  'python-httpx'
  'python-ollama'
)

makedepends=(
  'python-pip'
  'python-build'
  'python-installer'
  'python-wheel'
)

optdepends=(
  'python-questionary: interactive prompts'
  'ollama: for AI features'
  'jre-openjdk: backend service'
)

source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
cd "$srcdir/ArchAngel---An-AI-driven-CLI-Assistant-for-arch-based-sytems-$pkgver"
python -m build --wheel --no-isolation
}

package() {
  cd "$srcdir/ArchAngel---An-AI-driven-CLI-Assistant-for-arch-based-sytems-$pkgver"
  python -m installer --destdir="$pkgdir" dist/*.whl
}

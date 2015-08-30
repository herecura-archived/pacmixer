# Maintainer: Karol "Kenji Takahashi" Wozniak <wozniakk@gmail.com>

pkgname=pacmixer
pkgver=0.6.2
pkgrel=1
pkgdesc="alsamixer alike for PulseAudio."
arch=('i686' 'x86_64')
url="https://github.com/KenjiTakahashi/pacmixer"
license=('GPL3')
depends=(
    'ncurses'
    'libpulse'
    'gnustep-base'
)
makedepends=(
    'gcc-objc'
    'ninja'
)
source=("$pkgname-$pkgver.tar.gz::https://github.com/KenjiTakahashi/$pkgname/archive/$pkgver.tar.gz")
sha256sums=('6ffbcaa4abf5300e9e10bd0da78eef3e011741bd5509f32bd9f6b14250d27f94')

build() {
    cd "$pkgname-$pkgver"
    ./mk
}

package() {
    cd "$pkgname-$pkgver"
    DESTDIR="$pkgdir" PREFIX="/usr" ./mk install
}


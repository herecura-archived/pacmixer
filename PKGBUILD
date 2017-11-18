# Maintainer: Karol "Kenji Takahashi" Wozniak <wozniakk@gmail.com>

pkgname=pacmixer
pkgver=0.6.3
pkgrel=1
pkgdesc="alsamixer alike for PulseAudio."
arch=('x86_64')
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
sha256sums=('853bad75f57afa93df16902c78cc452bc79f3a38db5e0f6452cd10b3b07a5f7a')

build() {
    cd "$pkgname-$pkgver"
    ./mk
}

package() {
    cd "$pkgname-$pkgver"
    DESTDIR="$pkgdir" PREFIX="/usr" ./mk install
}


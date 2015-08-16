# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=Hmpf
pkgname=hmpf
pkgver=0.1
pkgrel=3
pkgdesc="An MPD client designed for a Home Theatre PC"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-configfile' 'haskell-crypto' 'haskell-http=4000.0.9' 'haskell-mtl' 'haskell-network=2.2.1.7' 'haskell-time=1.1.4' 'haskell-unix=2.4.0.2' 'haskell-utf8-string')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('6c9e36546ef1c940749d233dfbf7e85d')

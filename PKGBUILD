# Maintainer: Renato Garcia <fgarcia.renato@gmail.com>
# Contributor: Tiago Camargo <tcamargo@gmail.com>
# Contributor: Shinlun Hsieh <yngwiexx@yahoo.com.tw>

pkgname=stella
pkgver=3.8.1
pkgrel=1
pkgdesc='A multi-platform Atari 2600 VCS emulator'
arch=('i686' 'x86_64')
url='http://stella.sourceforge.net/'
license=('GPL')
depends=('gcc-libs' 'sdl' 'libpng')
source=("http://downloads.sourceforge.net/sourceforge/${pkgname}/${pkgname}-${pkgver}-src.tar.gz")
md5sums=('251f95b623158d0d63171f423eb2eaf2')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  make "DESTDIR=${pkgdir}" install
}

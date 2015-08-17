#Autor: Alexandre Minoshi(Almin-Soft Group)
#Maintainer: Alexandre Minoshi

pkgname=pacmanxg4
pkgver=4.11.3
pkgrel=1
pkgdesc="Yet another GUI for pacman and yaourt. Depends neither GTK nor Qt, only X11"
options=('!strip')
arch=('i686' 'x86_64')
url="http://almin-soft.nx0.ru/pacmanxg_4x_series.html"
license=('GPL2')
if [ "${CARCH}" = 'x86_64' ]; then
depends=('pacman' 'lib32-libx11' 'lib32-gcc-libs' 'lib32-libxft')
elif [ "${CARCH}" = 'i686' ]; then
depends=('pacman' 'libx11' 'gcc-libs')
fi
optdepends=('yaourt: AUR support' 'lib32-libxft: antialiased problem fix' 'pkgtools: pkgfile utility check')
install=${pkgname}.install
source=("http://almin-soft.nx0.ru/media/files/binaries/download.php?get=pacmanXG4.tar.bz2")

package() {
  install -d $pkgdir/opt/pacmanxg4
  install -Dm755 pacmanxg $pkgdir/opt/pacmanxg4/pacmanxg
  install -Dm755 langs/en.lang $pkgdir/opt/pacmanxg4/langs/en.lang
  install -Dm755 langs/rus.lang $pkgdir/opt/pacmanxg4/langs/ru.lang
  install -Dm755 dizz.sh $pkgdir/opt/pacmanxg4/dizz.sh
  install -Dm644 icon.png $pkgdir/usr/share/pixmaps/pacmanxg.png
  install -Dm644 pacmanxg4.desktop $pkgdir/usr/share/applications/pacmanxg4.desktop
  install -d $pkgdir/usr/bin/
}

md5sums=('cb09843662d0f6016967744a099c86a5')

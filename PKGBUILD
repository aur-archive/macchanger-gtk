# Maintainer: archtux <antonio dot arias99999 at gmail dot com>

pkgname=macchanger-gtk
pkgver=1.1
pkgrel=4
pkgdesc="GUI for manipulating the MAC address of network interfaces."
arch=('any')
url="http://packages.debian.org/sid/macchanger-gtk"
license=('GPL2')
depends=('glade-perl' 'glib-perl' 'libui-dialog-perl' 'macchanger' 'zenity')
install=$pkgname.install
source=(http://ftp.de.debian.org/debian/pool/main/m/$pkgname/${pkgname}_1.1.orig.tar.gz
        $pkgname.install)
md5sums=('36c8bdbb647e0e686a8dc838f6316d89'
         'ce1a9d7df5de1447d30bc96c561a2b8a')

package() {
  cd $srcdir/$pkgname-$pkgver

  # Fix syntax errors
  sed -i 's_Known vendedor_Known vendors_' glade/$pkgname.glade
  sed -i 's_Know vendedor_Known vendors_' glade/$pkgname.glade

  install -Dm755 $pkgname $pkgdir/usr/bin/$pkgname
  install -Dm644 glade/$pkgname.glade $pkgdir/usr/share/$pkgname/$pkgname.glade
}
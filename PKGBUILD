pkgname=kdeplasma-addons-applets-smooth-tasks2
_pkgname=smooth-tasks
pkgver=20120213
pkgrel=2
pkgdesc="Smooth-tasks with support new KDE 4.8 API's"
url="http://kde-look.org/content/show.php/Smooth+Tasks+2?content=148813"
arch=('i686' 'x86_64')
license=('GPL2')
source=("http://beonis.fr/${_pkgname}-v2012-02-13.tar.gz")
md5sums=('17ad41297fbf31cbd48360e17c6494a4')
depends=('kdebase-workspace')
makedepends=('cmake')
provides=('eplasma-addons-applets-smooth-tasks')
conflicts=('eplasma-addons-applets-smooth-tasks')

build() {
  cd "${srcdir}"
  cmake . -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd "${srcdir}"
  make DESTDIR="${pkgdir}" install
}
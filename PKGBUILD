# Maintainer: speps <speps dot aur dot archlinux dot org>

pkgname=rssguard-qt4
pkgver=2.0.0.4
pkgrel=1
pkgdesc="A simple (yet powerful) Qt4 feed reader."
arch=('i686' 'x86_64')
url="https://bitbucket.org/skunkos/rssguard"
license=('GPL3')
depends=('qtwebkit')
makedepends=('cmake')
provides=('rss-guard' 'rssguard')
conflicts=('rss-guard' 'rssguard')
replaces=('rss-guard')
install="$pkgname.install"
source=("$url/downloads/rssguard-$pkgver.tar.gz")
md5sums=('780a6657237d2dc32d7dc486753affc3')

prepare() {
  cd rssguard-$pkgver
  [ -d b ] || mkdir b
}

build() {
  cd rssguard-$pkgver/b
  cmake .. -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd rssguard-$pkgver/b
  make DESTDIR="$pkgdir/" install
}

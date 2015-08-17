# Maintainer: guillaume bouchard <guillaum.bouchard@gmail.com>
pkgname=python3-jedi-git
pkgver=20130117
pkgrel=1
pkgdesc="Python auto completion library"
arch=(any)
url="https://github.com/davidhalter/jedi"
license=('LGPL')
depends=('python3')
makedepends=('git python-distribute')

_gitroot="https://github.com/davidhalter/jedi.git"
_gitname="jedi"

build() {
  if [ -d $_gitname ] ; then
    cd $_gitname && git pull origin
  else
    git clone $_gitroot $_gitname
  fi
  
  cd "$srcdir/jedi"

  python setup.py install --prefix=/usr --root="$pkgdir" || return 1

}

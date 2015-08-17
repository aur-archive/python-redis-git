# Maintainer: lilydjwg <lilydjwg@gmail.com>
# Contributor: Felipe Morales <hel.sheep@gmail.com>
# Based on the packaging of Frank Smit <frank@61924.nl> (redis-py-git on AUR)

_gitname=redis-py
pkgname=python-redis-git
pkgver=2.9.1.6_ga5dbfc1
pkgrel=1
pkgdesc='Redis Python Client'
arch=('any')
url='https://github.com/andymccurdy/redis-py'
license=('MIT')
depends=('python' 'redis')
makedepends=('git' 'python-setuptools')
source=('git://github.com/andymccurdy/redis-py.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git describe --tags | sed 's/-/./;s/-/_/g'
}

package() {
  cd "$srcdir/$_gitname"
  python3 setup.py install --root="$pkgdir/" --optimize=1
}


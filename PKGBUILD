pkgname=luajit
pkgver=2.0.5
pkgrel=1
pkgdesc='Just-in-time compiler and drop-in replacement for Lua 5.1'
arch=('x86_64')
url='http://luajit.org/'
license=('MIT')
depends=('gcc-libs')
source=(http://luajit.org/download/LuaJIT-$pkgver.tar.gz)
md5sums=('48353202cbcacab84ee41a5a70ea0a2c')

build() {
  cd LuaJIT-$pkgver
  make amalg PREFIX=/usr
}

package() {
  cd LuaJIT-$pkgver
  make install DESTDIR="$pkgdir" PREFIX=/usr

  install -Dm644 COPYRIGHT "$pkgdir"/usr/share/licenses/$pkgname/COPYRIGHT
}

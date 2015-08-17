# Maintainer: Niels Abspoel <aboe76(at)gmail(dot)comme>
# Last version visible on https://github.com/dotless-de/vagrant-vbguest
pkgname=vagrant-vbguest
pkgver=0.6.4
pkgrel=1
pkgdesc="a plugin which automatically installs the host's VirtualBox Guest Additions on the guest system."
arch=(any)
url="https://github.com/dotless-de/vagrant-vbguest"
arch=('x86_64' 'i686')
license=('MIT')
makedepends=('rubygems' 'rake')
makedepends=('rubygems' 'rake')
depends=('vagrant>=1.0.0' \
         'ruby' \
         'virtualbox>=4.0' \
         'virtualbox-guest-iso>=4.0' \
         'ruby-archive-tar-minitar' \
         'ruby-micromachine' \
         'ruby-net-ssh-2.2' \
         'ruby-net-scp' \
         'ruby-erubis' \
         'ruby-i18n' \
         'ruby-log4r' \
         'ruby-childprocess')
source=(http://rubygems.org/downloads/${pkgname}-${pkgver}.gem)
noextract=($pkgname-$pkgver.gem)

build() {
  cd $srcdir
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies \
    -i "$pkgdir$_gemdir" -n "$pkgdir"/usr/bin $pkgname-$pkgver.gem
}
md5sums=('2da2e8f9915a1d267d51257dbb2665ae')

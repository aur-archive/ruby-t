# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: uberushaximus <uberushaximus AT gmail DOT com>

_gemname=t
pkgname=ruby-$_gemname
pkgver=2.5.0
pkgrel=1
pkgdesc='CLI for Twitter'
arch=(any)
url='http://sferik.github.com/t/'
license=(MIT)
depends=(ruby ruby-launchy ruby-geokit ruby-htmlentities ruby-oauth ruby-retryable ruby-thor ruby-twitter)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('ef95d6845c3ba9e6e89d829f0a6294855c5a8948')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}

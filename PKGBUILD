# Maintainer: lilydjwg <lilydjwg@gmail.com>
pkgname=wait-online
pkgver=0.2
pkgrel=1
pkgdesc="tools to wait for Internet (204 response)"
arch=('any')
license=("GPLv3")
depends=('python-systemd')
source=(
  check-online
  wait-online
  tmpfiles.conf
  wait-online.service
  wait-online-onresume.service
)

sha1sums=('2ed9dcf07dd9a427a62e151ae4ee34c696e53d2c'
          'b0d83c0c046764331a6625d3027f3102aa632412'
          '3f861ed5cf7bd2820dee66f6b575852418deeea0'
          '8707500e28807069579f9740cad675985f5dd69b'
          '4ea5880b28933efe01f0461916ddef0f01d23efa')

build() {
  true
}

package() {
  cd "${srcdir}"
  install -Dm755 wait-online "${pkgdir}/usr/bin/wait-online"
  install -Dm755 check-online "${pkgdir}/usr/bin/check-online"
  install -Dm644 wait-online.service "${pkgdir}/usr/lib/systemd/system/wait-online.service"
  install -Dm644 wait-online-onresume.service "${pkgdir}/usr/lib/systemd/system/wait-online-onresume.service"
  install -Dm644 tmpfiles.conf "${pkgdir}/usr/lib/tmpfiles.d/${pkgname}.conf"
}

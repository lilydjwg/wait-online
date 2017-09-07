# Maintainer: lilydjwg <lilydjwg@gmail.com>
pkgname=wait-204
pkgver=0.1
pkgrel=1
pkgdesc="tools to wait for the Internet (204 response)"
arch=('any')
license=("GPLv3")
depends=('python-systemd')
source=(
  check-204
  wait-204
  tmpfiles.conf
  wait-204.service
  wait-204-restart.service
)

sha1sums=('0baf1afe964cc117987cc9fd609ecb64ba4f7d23'
          'f619942aab05e39a783917c2eaf25d0a16937440'
          'b09328bb02cb3d7319d9e5e1555c3f74fc06fe77'
          'd14cf59303b94bd4b92e12411b012681ab0c3033'
          '86cd625d209a78e6397c9ebefc2c793524c3ebfa')

build() {
  true
}

package() {
  cd "${srcdir}"
  install -Dm755 wait-204 "${pkgdir}/usr/bin/wait-204"
  install -Dm755 check-204 "${pkgdir}/usr/bin/check-204"
  install -Dm644 wait-204.service "${pkgdir}/usr/lib/systemd/system/wait-204.service"
  install -Dm644 wait-204-restart.service "${pkgdir}/usr/lib/systemd/system/wait-204-restart.service"
  install -Dm644 tmpfiles.conf "${pkgdir}/usr/lib/tmpfiles.d/${pkgname}.conf"
}

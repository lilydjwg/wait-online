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

sha1sums=('ac7989bd662090b1ab35138a1e141290b83cddce'
          '03acb327394e587ecf4bcf0da33b1c875741e1f9'
          'b09328bb02cb3d7319d9e5e1555c3f74fc06fe77'
          'd65c00d77621567bc79039024500782de3c1c57d'
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

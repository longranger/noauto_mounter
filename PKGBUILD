# Maintainer: longranger <longranger dot 406 at gmail dot com>
pkgname="noauto_mounter"
pkgver="0.2"
pkgrel=1
pkgdesc="auto mount local and nfs noauto fstab mounts"
arch=('x86_64')
url="https://github.com/longranger/noauto_mounter"
license=('GPL')
depends=()
makedepends=('git')
source=("${pkgname}-${pkgver}"::'git://github.com/longranger/noauto_mounter')
md5sums=('SKIP')
install='noauto_mounter.install'

pkgver() {
	cd "${pkgname}"
	# Using the most recent annotated tag reachable from the last commit:
	git describe --long | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}
package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -Dm755 noauto_mounter "${pkgdir}"/usr/bin/noauto_mounter
	install -Dm755 noauto_mounter.timer "${pkgdir}"/etc/systemd/system/noauto_mounter.timer
	install -Dm755 noauto_mounter.service "${pkgdir}"/etc/systemd/system/noauto_mounter.service
}

# Maintainer: Chaiwat Suttipongsakul <cwt@bashell.com>

pkgname=k1x-vpu-firmware
pkgdesc="Video Process Unit firmware for SpacemiT K1-x"
pkgver=2.0.2
pkgrel=1
arch=('riscv64')
url="https://gitee.com/bianbu-linux/k1x-vpu-firmware"
license=('BSD-3-Clause')
_tag=v${pkgver}
_srcname=${pkgname}-${_tag}
options=('!strip' '!debug')
source=("${_srcname}.tar.gz::${url}/repository/archive/${_tag}.tar.gz")

b2sums=('c97807557344e2cccc7de0e2653abf119ded174b2f4719a9aef39e28a4750b8f2aae50c51af02a87244c93b23f1073a7bebfb11fa6edf2c18ec59e1b5963bead')

package() {
    mkdir -p ${pkgdir}/usr/lib/firmware
    cd ${srcdir}/${_srcname}/lib/firmware
    cp -a linlon-v52_v76-80-2 ${pkgdir}/usr/lib/firmware/
    install -Dm644 ${srcdir}/${_srcname}/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}


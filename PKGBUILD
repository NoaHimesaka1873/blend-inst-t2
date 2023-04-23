pkgname='blend-inst-t2'
pkgver=1.0r1
pkgrel=1
pkgdesc='blendOS Installer Framework for Macs with T2 chip'
arch=(any)
depends=('squashfs-tools' 'arch-install-scripts' 'util-linux' 'parted')
provides=('blend-inst')
conflicts=('blend-inst')
source=('git-inst::git+https://github.com/NoaHimesaka1873/blend-inst-t2.git')
sha256sums=('SKIP')

pkgver() {
    cd "${srcdir}/git-inst"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "${srcdir}/git-inst"
    install -Dm755 blend-inst -t "${pkgdir}/usr/bin/"
}

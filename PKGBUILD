# Maintainer: Your Name <your.email@example.com>
pkgname=nicoed
pkgver=1.0.0
pkgrel=1
pkgdesc="A configuration editor for the Niri Wayland compositor"
arch=('any')
url="https://github.com/your-username/nicoed"
license=('MIT')
depends=('python' 'tk')
source=("nicoed.py"
        "nicoed.desktop")
sha256sums=('SKIP'
            'SKIP')

package() {
    # Install the main script
    install -Dm755 "nicoed.py" "${pkgdir}/usr/bin/nicoed"

    # Install the desktop file
    install -Dm644 "nicoed.desktop" "${pkgdir}/usr/share/applications/nicoed.desktop"
}

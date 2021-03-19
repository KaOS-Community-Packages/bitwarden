pkgname=bitwarden
pkgver=1.25.1
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('b20c5c3890a98f6990f7e7f1274027aba3011a416781b6fd76b6c37959ebf787cdb129dd16fe9b4601b5cbc39018dadc36efe680391c04ed0a4c763d221a3cbd')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

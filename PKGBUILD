pkgname=bitwarden
pkgver=1.26.3
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('b7e6b96ced59ed936a80679aabecf40ae601972dcee6ae192a70f972de25a39d39b0e3f8ac59812f527e8d6f26c30859a47cc5231ca7020013ad07ee6a95a224')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

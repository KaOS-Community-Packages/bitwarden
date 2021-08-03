pkgname=bitwarden
pkgver=1.27.1
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('92a6a5d3d64a17ddf2b742d9328adf27566da466c9c4d22fff910eb9dabeda77f65fad07424e6abc8c4cace04c365ada84588d05270a5cf615eda36a5741e81c')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

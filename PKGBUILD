pkgname=bitwarden
pkgver=1.25.0
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('17d68cd9aae39bc8cd5b597e79d2e781fb46699f9c792fe36e453167699f528dc7ee35107626b4557dd70fcf27f35751a31b3015ed66a5d69b1b96128d95bf1b')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

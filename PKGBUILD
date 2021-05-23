pkgname=bitwarden
pkgver=1.26.4
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('b0de7ed7b00b5308a2137b2632150bd288a7383a13295814c6c6af1a85f911a6790ad162f67af07844f8fca80044b95f58a37e6ab762429d061f3c9af3616e11')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

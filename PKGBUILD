pkgname=bitwarden
pkgver=1.29.1
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('0c123e03eefe8d723ddfebc6e4733b2dcefd969407ed15023c164722262c2e0e65150f3457b7c65e6092618123ebea5fd5104673ff1e44a920a03cca73e4b592')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

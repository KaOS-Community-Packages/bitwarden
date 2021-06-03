pkgname=bitwarden
pkgver=1.26.5
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=()
license=('GPL-3')
options=('!strip' '!emptydirs')
source=("https://github.com/bitwarden/desktop/releases/download/v${pkgver}/Bitwarden-${pkgver}-amd64.deb")
sha512sums=('c2506a9f64d47138e6ce53bb7211e2562f9bb9847f4b48b059dd504eec312f6852571aaa550830f54488c0d67d02c0eb67bcac049a688098d1b8a55492b008f7')

package() {
	bsdtar -xf data.tar.xz -C "${pkgdir}/" 
	#Correct rights
	chmod 4755 "${pkgdir}/opt/Bitwarden/chrome-sandbox"
}

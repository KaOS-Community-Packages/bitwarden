pkgname=bitwarden
_pkgname=Bitwarden
pkgver=2023.9.3
pkgrel=1
pkgdesc='Open source password management solutions for individuals, teams, and business organizations.'
arch=('x86_64')
url="https://bitwarden.com/"
depends=('libnotify' 'libsecret' 'libxtst' 'libxss' 'nss')
license=('unknown' 'GPL-3')
source=("${pkgname}-${pkgver}.rpm::https://github.com/bitwarden/clients/releases/download/desktop-v${pkgver}/Bitwarden-${pkgver}-x86_64.rpm")
sha512sums=('SKIP')


build() {
	bsdtar -xf ${pkgname}-${pkgver}.rpm
}

package() {
	install -dm755 ${pkgdir}/opt/${_pkgname}
	install -dm755 ${pkgdir}/usr/bin
	install -dm755 ${pkgdir}/usr/lib/${pkgname}
	install -dm755 ${pkgdir}/etc
	install -dm755 ${pkgdir}/usr/share/icons/hicolor
	install -dm755 ${pkgdir}/usr/share/applications
	install -dm755 ${pkgdir}/usr/share/licenses
	install -Dm777 usr/share/applications/${pkgname}.desktop -t ${pkgdir}/usr/share/applications
	cp -a usr/share/icons/hicolor/* -t ${pkgdir}/usr/share/icons/hicolor
	install -Dm777 opt/${_pkgname}/bitwarden -t ${pkgdir}/usr/bin
	install -Dm777 opt/${_pkgname}/{chrome-sandbox,chrome_crashpad_handler,icudtl.dat,libEGL.so,libffmpeg.so,libGLESv2.so,libvk_swiftshader.so,libvulkan.so.1} -t \
	${pkgdir}/usr/lib/${pkgname}
	install -Dm755 opt/${_pkgname}/{LICENSE.electron.txt,LICENSES.chromium.html} -t ${pkgdir}/usr/share/licenses
	install -Dm755 opt/${_pkgname}/vk_swiftshader_icd.json ${pkgdir}/etc/bitwarden-vk_swiftshader_icd.json
	cp -a opt/${_pkgname} ${pkgdir}/opt/
	cp -a usr/share ${pkgdir}/usr
	chmod 0777 ${pkgdir}/opt/${_pkgname}/{chrome-sandbox,chrome_crashpad_handler}
}

# Maintainer : Echoes

pkgname=skystream
pkgver=2.9.0
pkgrel=1
pkgdesc="Free Movies & TV-Series Streaming App"
arch=("x86_64")
url="https://github.com/akashdh11/skystream"
licence=("GLP-3.0-only")
depends=("libvlc" "webkit2gtk-4.1" "gtk3" "libsecret")
source=("skystream.tar.gz::https://github.com/akashdh11/skystream/releases/download/v${pkgver}/skystream-linux-x64-v${pkgver}.tar.gz"
"Licence::https://github.com/akashdh11/skystream/blob/master/LICENSE"
)
sha256sums=('8421d108d98989cb4a865ee4548e711847eda0d094dfe7299734dfe8ffeed46c'
            'b509c8a2a2d40b53ae22d2331ce2f0a555342cdecba58542bda58ea084460955')

package() {
	install -d "$pkgdir/opt/skystream"
	(
		cd "$pkgdir/opt/skystream"
		bsdtar -xzf "$srcdir/skystream.tar.gz"
	)
	
	chmod 755 "$pkgdir/opt/skystream/skystream"
	install -Dm644 "$startdir/skystream.png" "$pkgdir/usr/share/pixmaps/skystream.png"

	install -Dm755 "$startdir/usr/bin/skystream" "$pkgdir/usr/bin/skystream"
	install -Dm644 "$startdir/usr/share/applications/skystream.desktop" "$pkgdir/usr/share/applications/skystream.desktop"
	install -Dm644 "$srcdir/Licence" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

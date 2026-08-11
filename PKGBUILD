# Maintainer: Your Name <email>
pkgname=zotero-wpsjs
pkgver=1.7.23                 # 手动指定
pkgrel=1
pkgdesc="Zotero plugin for WPS Office (JS) - Linux installer"
arch=('any')
url="https://gitee.com/wangrui5015/Zotero-WPSJS"
license=('GPL')
depends=('zotero' 'python' 'wps-office-cn')
makedepends=()
# 使用压缩包，不需要 git
source=("$pkgname-$pkgver.tar.gz::https://gitee.com/wangrui5015/Zotero-WPSJS/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('SKIP')          # 可以先用 SKIP，后续用 updpkgsums 生成
install="$pkgname.install"

package() {
  cd "$srcdir/Zotero-WPSJS-v$pkgver"
  # 只复制 Linux 文件夹
  install -dm755 "$pkgdir/usr/share/$pkgname"
  cp -r Linux/* "$pkgdir/usr/share/$pkgname/"
  chmod +x "$pkgdir/usr/share/$pkgname/"*.py
}

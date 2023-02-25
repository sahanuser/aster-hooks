# Maintainer: Sahan Rasanjana <sahan.user@gmail.com>
pkgname=aster-hooks
pkgver=1
pkgrel=6
pkgdesc='Aster Linux pacman hooks'
arch=('any')
license=('GPL3')
url="https://github.com/asterlinux/aster-hooks"
depends=(libnotify)

source=(
  aster-os-release.hook
  aster-lsb-release.hook
  aster-hooks.hook
  aster-hooks-runner
  aster-reboot-required
  aster-reboot-required.hook
  grub-update.hook
  plymouth-update.hook
)
sha512sums=('SKIP'
	    'SKIP'
	    'SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
	    'SKIP'
            'SKIP')
package() {
  local hooks=$pkgdir/usr/share/libalpm/hooks
  local bin=$pkgdir/usr/bin

  install -Dm644 aster-lsb-release.hook      $hooks/aster-lsb-release.hook
  install -Dm644 aster-os-release.hook       $hooks/aster-os-release.hook
  install -Dm644 aster-hooks.hook            $hooks/aster-hooks.hook
  install -Dm644 aster-reboot-required.hook  $hooks/aster-reboot-required.hook
  install -Dm755 aster-reboot-required       $bin/aster-reboot-required
  install -Dm755 aster-hooks-runner          $bin/aster-hooks-runner
  install -Dm644 grub-update.hook            $hooks/grub-update.hook
  install -Dm644 plymouth-update.hook        $hooks/plymouth-update.hook
}

# Maintainer: Sahan Rasanjana <sahan.user@gmail.com>

pkgname=aster-hooks
pkgver=1
pkgrel=5
pkgdesc='Aster Linux pacman hooks'
arch=('any')
license=('GPL3')
url="https://github.com/asterlinux/aster-hooks"
depends=(libnotify)

source=(
  asl-os-release.hook
  asl-lsb-release.hook
  asl-hooks.hook
  asl-hooks-runner
  asl-reboot-required
  asl-reboot-required.hook
  grub-update.hook
)
sha512sums=('SKIP'
	    'SKIP'
	    'SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
	    'SKIP')
package() {
  local hooks=$pkgdir/usr/share/libalpm/hooks
  local bin=$pkgdir/usr/bin

  install -Dm644 asl-lsb-release.hook      $hooks/asl-lsb-release.hook
  install -Dm644 asl-os-release.hook       $hooks/asl-os-release.hook
  install -Dm644 asl-hooks.hook           $hooks/asl-hooks.hook
  install -Dm644 asl-reboot-required.hook  $hooks/asl-reboot-required.hook
  install -Dm755 asl-reboot-required       $bin/asl-reboot-required
  install -Dm755 asl-hooks-runner         $bin/asl-hooks-runner
  install -Dm644 grub-update.hook           $hooks/grub-update.hook
}

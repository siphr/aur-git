# Maintainer: siphr <archlinux@techtum.dev>
pkgname=aur-git
pkgver=0.0.1
pkgrel=1
pkgdesc="Retrieve and install package an AUR package."
depends=(python)
arch=(x86_64)
source=("https://github.com/siphr/aur-git.git")
license=('MIT')
install=.install

build() {
    echo "echo `date`" > aur-git
    echo "python -m aur_git \$@" >> aur-git
}

package() {
    mkdir -p $pkgdir/usr/bin
    cp "$srcdir/aur-git" "$pkgdir/usr/bin/aur-git"
    chmod +x $pkgdir/usr/bin/aur-git
    echo 'Finished setting up aur-git.'
}

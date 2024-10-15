pkgname=wmenu-git
pkgver=0.1.9
pkgrel=1
arch=("x86_64")
depens=("cairo" "pango" "libxkbcommon" "wayland")
makedepens=("meson" "ninja" "scdoc")


build() {
    cd ${srcdir}/..
    meson setup build_release --buildtype=release --reconfigure
    meson compile -C build_release
}

package() {
    cd ${srcdir}/..
    meson install -C build_release --destdir ${pkgdir}
}

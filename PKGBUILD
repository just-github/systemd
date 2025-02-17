# Maintainer: Philip Müller <philm[at]manjaro[dot]org>
# Maintainer: Bernhard Landauer <bernhard[at]manjaro[dot]org>
# Maintainer: Mark Wagie <mark at manjaro dot org>
# Contributor: Helmut Stult
# Contributor: Christian Hesse <mail@eworm.de>

pkgbase=systemd
pkgname=('systemd'
         'systemd-libs'
         'systemd-resolvconf'
         'systemd-sysvcompat'
         'systemd-ukify')
_tag='256.6'
# Upstream versioning is incompatible with pacman's version comparisons, one
# way or another. So we replace dashes and tildes with the empty string to
# make sure pacman's version comparing does the right thing for rc versions:
pkgver="${_tag/[-~]/}"
pkgrel=1
arch=('x86_64')
license=('LGPL-2.1-or-later')
url='https://www.github.com/systemd/systemd'
makedepends=('acl' 'cryptsetup' 'docbook-xsl' 'gperf' 'lz4' 'xz' 'pam' 'libelf'
             'intltool' 'iptables' 'kmod' 'libarchive' 'libcap' 'libidn2' 'libgcrypt'
             'libmicrohttpd' 'libxcrypt' 'libxslt' 'util-linux' 'linux-api-headers'
             'python-jinja' 'python-lxml' 'quota-tools' 'shadow' 'git'
             'meson' 'libseccomp' 'pcre2' 'audit' 'kexec-tools' 'libxkbcommon'
             'bash-completion' 'p11-kit' 'systemd' 'libfido2' 'tpm2-tss' 'rsync'
             'bpf' 'libbpf' 'clang' 'llvm' 'curl' 'gnutls' 'python-pyelftools'
             'libpwquality' 'qrencode' 'lib32-gcc-libs' 'python-pefile')
conflicts=("mkinitcpio<38-1")
validpgpkeys=('63CDA1E5D3FC22B998D20DD6327F26951A015CC4'  # Lennart Poettering <lennart@poettering.net>
              'A9EA9081724FFAE0484C35A1A81CEA22BC8C7E2E'  # Luca Boccassi <luca.boccassi@gmail.com>
              '9A774DB5DB996C154EBBFBFDA0099A18E29326E1'  # Yu Watanabe <watanabe.yu+github@gmail.com>
              '5C251B5FC54EB2F80F407AAAC54CA336CFEB557E') # Zbigniew Jędrzejewski-Szmek <zbyszek@in.waw.pl>
source=("git+https://github.com/systemd/systemd#tag=v${_tag}?signed"
        '0001-Use-Arch-Linux-device-access-groups.patch'
        # bootloader files
        'manjaro.conf'
        'loader.conf'
        'splash-manjaro.bmp'
        # pam configuration
        'systemd-user.pam'
        # pacman / libalpm hooks
        'systemd-hook'
        '20-systemd-sysusers.hook'
        '30-systemd-binfmt.hook'
        '30-systemd-catalog.hook'
        '30-systemd-daemon-reload-system.hook'
        '30-systemd-daemon-reload-user.hook'
        '30-systemd-hwdb.hook'
        '30-systemd-sysctl.hook'
        '30-systemd-tmpfiles.hook'
        '30-systemd-udev-reload.hook'
        '30-systemd-update.hook')
sha512sums=('e9fc19946f329aa89c1014a735d4d7828cebaa32ece8244b79e101c41d1c0cb0207b4109ce55d14204b0915f6cac57ace6286c6abaebd809031949693131de16'
            '3ccf783c28f7a1c857120abac4002ca91ae1f92205dcd5a84aff515d57e706a3f9240d75a0a67cff5085716885e06e62597baa86897f298662ec36a940cf410e'
            '72dfd0e513e61f391d2b0bf8d9f13c6e2d2732dd7bd52413dccc791c562ab6265062c17d5abe60a42db0775e0b2352eba5e18d14fa2740c176d82edac4867c32'
            '363052706e8fdb040754d0bdc75377212865314ffb8718f8889e6c8a0049ea6cc442cb34fb9a204622eca597b78a547421867cb7517bd1b7342badee581bde7d'
            '6200f2844bdcd230ef4efd27313a92b663a199fe7b3cf1794d17ca4d62bb2d7e9856e6a6e2ea0b912955df124c9d97374c70ae4ef2ff092b25296769fe9e8ba7'
            'b90c99d768dc2a4f020ba854edf45ccf1b86a09d2f66e475de21fe589ff7e32c33ef4aa0876d7f1864491488fd7edb2682fc0d68e83a6d4890a0778dc2d6fe19'
            '3cb8f88c1bffc753d0c540be5d25a0fdb9224478cca64743b5663340f2f26b197775286e6e680228db54c614dcd11da1135e625674a622127681662bec4fa886'
            '299dcc7094ce53474521356647bdd2fb069731c08d14a872a425412fcd72da840727a23664b12d95465bf313e8e8297da31259508d1c62cc2dcea596160e21c5'
            '0d6bc3d928cfafe4e4e0bc04dbb95c5d2b078573e4f9e0576e7f53a8fab08a7077202f575d74a3960248c4904b5f7f0661bf17dbe163c524ab51dd30e3cb80f7'
            '2b50b25e8680878f7974fa9d519df7e141ca11c4bfe84a92a5d01bb193f034b1726ea05b3c0030bad1fbda8dbb78bf1dc7b73859053581b55ba813c39b27d9dc'
            'a436d3f5126c6c0d6b58c6865e7bd38dbfbfb7babe017eeecb5e9d162c21902cbf4e0a68cf3ac2f99815106f9fa003b075bd2b4eb5d16333fa913df6e2f3e32a'
            '190112e38d5a5c0ca91b89cd58f95595262a551530a16546e1d84700fc9644aa2ca677953ffff655261e8a7bff6e6af4e431424df5f13c00bc90b77c421bc32d'
            'a1661ab946c6cd7d3c6251a2a9fd68afe231db58ce33c92c42594aedb5629be8f299ba08a34713327b373a3badd1554a150343d8d3e5dfb102999c281bd49154'
            '9426829605bbb9e65002437e02ed54e35c20fdf94706770a3dc1049da634147906d6b98bf7f5e7516c84068396a12c6feaf72f92b51bdf19715e0f64620319de'
            'da7a97d5d3701c70dd5388b0440da39006ee4991ce174777931fea2aa8c90846a622b2b911f02ae4d5fffb92680d9a7e211c308f0f99c04896278e2ee0d9a4dc'
            'a50d202a9c2e91a4450b45c227b295e1840cc99a5e545715d69c8af789ea3dd95a03a30f050d52855cabdc9183d4688c1b534eaa755ebe93616f9d192a855ee3'
            '825b9dd0167c072ba62cabe0677e7cd20f2b4b850328022540f122689d8b25315005fa98ce867cf6e7460b2b26df16b88bb3b5c9ebf721746dce4e2271af7b97')

_meson_version="${pkgver}-${pkgrel}"
_meson_vcs_tag='false'
_meson_mode='release'
_meson_compile=()
_meson_install=()

if ((_systemd_UPSTREAM)); then
  _meson_version="${pkgver}"
  _meson_vcs_tag='true'
  _meson_mode='developer'
  pkgname+=('systemd-tests')
  if ((_systemd_QUIET)); then
    _meson_install=('--quiet')
  else
    _meson_compile=('--verbose')
  fi
fi

_backports=(
)

_reverts=(
)

prepare() {
  cd "${pkgbase}"

  local _c _l
  for _c in "${_backports[@]}"; do
    if [[ "${_c}" == *..* ]]; then _l='--reverse'; else _l='--max-count=1'; fi
    git log --oneline "${_l}" "${_c}"
    git cherry-pick --mainline 1 --no-commit "${_c}"
  done
  for _c in "${_reverts[@]}"; do
    if [[ "${_c}" == *..* ]]; then _l='--reverse'; else _l='--max-count=1'; fi
    git log --oneline "${_l}" "${_c}"
    git revert --mainline 1 --no-commit "${_c}"
  done

  # Replace cdrom/dialout/tape groups with optical/uucp/storage
  patch -Np1 -i ../0001-Use-Arch-Linux-device-access-groups.patch
}

build() {
  local _timeservers=({0..3}.manjaro.pool.ntp.org)
  local _nameservers=(
    # We use these public name services, ordered by their privacy policy (hopefully):
    #  * Cloudflare (https://1.1.1.1/)
    #  * Quad9 (https://www.quad9.net/)
    #  * Google (https://developers.google.com/speed/public-dns/)
    '1.1.1.1#cloudflare-dns.com'
    '9.9.9.9#dns.quad9.net'
    '8.8.8.8#dns.google'
    '2606:4700:4700::1111#cloudflare-dns.com'
    '2620:fe::9#dns.quad9.net'
    '2001:4860:4860::8888#dns.google'
  )

  local _meson_options=(
    -Dversion-tag="${_meson_version}-manjaro"
    -Dvcs-tag="${_meson_vcs_tag}"
    -Dshared-lib-tag="${_meson_version}"
    -Dmode="${_meson_mode}"

    -Dapparmor=disabled
    -Dbootloader=enabled
    -Dxenctrl=disabled
    -Dbpf-framework=enabled
    -Dima=false
    -Dinstall-tests=true
    -Dlibidn2=enabled
    -Dlz4=enabled
    -Dman=enabled
    -Dnscd=false
    -Dselinux=disabled

    # We disable DNSSEC by default, it still causes trouble:
    # https://github.com/systemd/systemd/issues/10579

    -Ddbuspolicydir=/usr/share/dbus-1/system.d
    -Ddefault-dnssec=no
    -Ddefault-hierarchy=unified
    -Ddefault-kill-user-processes=false
    -Ddefault-locale='C.UTF-8'
    -Dlocalegen-path=/usr/bin/locale-gen
    -Ddns-over-tls=openssl
    -Dfallback-hostname='manjaro'
    -Dnologin-path=/usr/bin/nologin
    -Dntp-servers="${_timeservers[*]}"
    -Ddns-servers="${_nameservers[*]}"
    -Drpmmacrosdir=no
    -Dsysvinit-path=
    -Dsysvrcnd-path=

    -Dsbat-distro='manjaro'
    -Dsbat-distro-summary='Manjaro Linux'
    -Dsbat-distro-pkgname="${pkgname}"
    -Dsbat-distro-version="${pkgver}"
    -Dsbat-distro-url="https://gitlab.manjaro.org/packages/core/${pkgname}/"
    -Dsupport-url='https://forum.manjaro.org/c/support'
  )

  arch-meson "${pkgbase}" build "${_meson_options[@]}" $MESON_EXTRA_CONFIGURE_OPTIONS

  meson compile -C build "${_meson_compile[@]}"
}

check() {
  meson test -C build --print-errorlogs
}

package_systemd() {
  pkgdesc='system and service manager'
  license+=(
    'CC0-1.0' # siphash
    'GPL-2.0-or-later' # udev
    'MIT-0' # documentation and config files
  )
  depends=("systemd-libs=${pkgver}"
           'acl' 'libacl.so' 'bash' 'cryptsetup' 'libcryptsetup.so' 'dbus'
           'dbus-units' 'kbd' 'kmod' 'hwdata' 'libcap' 'libcap.so'
           'libgcrypt' 'libxcrypt' 'libcrypt.so' 'libidn2' 'lz4' 'pam'
           'libelf' 'libseccomp' 'libseccomp.so' 'util-linux' 'libblkid.so'
           'libmount.so' 'xz' 'pcre2' 'audit' 'libaudit.so'
           'openssl' 'libcrypto.so' 'libssl.so')
  provides=('nss-myhostname' "systemd-tools=$pkgver" "udev=$pkgver")
  replaces=('nss-myhostname' 'systemd-tools' 'udev')
  conflicts=('nss-myhostname' 'systemd-tools' 'udev')
  optdepends=('libmicrohttpd: systemd-journal-gatewayd and systemd-journal-remote'
              'quota-tools: kernel-level quota management'
              'systemd-sysvcompat: symlink package to provide sysvinit binaries'
              'systemd-ukify: combine kernel and initrd into a signed Unified Kernel Image'
              'polkit: allow administration as unprivileged user'
              'curl: systemd-journal-upload, machinectl pull-tar and pull-raw'
              'gnutls: systemd-journal-gatewayd and systemd-journal-remote'
              'qrencode: show QR codes'
              'iptables: firewall features'
              'libarchive: convert DDIs to tarballs'
              'libbpf: support BPF programs'
              'libpwquality: check password quality'
              'libfido2: unlocking LUKS2 volumes with FIDO2 token'
              'libp11-kit: support PKCS#11'
              'tpm2-tss: unlocking LUKS2 volumes with TPM2')
  backup=(etc/pam.d/systemd-user
          etc/systemd/coredump.conf
          etc/systemd/homed.conf
          etc/systemd/journald.conf
          etc/systemd/journal-remote.conf
          etc/systemd/journal-upload.conf
          etc/systemd/logind.conf
          etc/systemd/networkd.conf
          etc/systemd/oomd.conf
          etc/systemd/pstore.conf
          etc/systemd/resolved.conf
          etc/systemd/sleep.conf
          etc/systemd/system.conf
          etc/systemd/timesyncd.conf
          etc/systemd/user.conf
          etc/udev/iocost.conf
          etc/udev/udev.conf)
  install=systemd.install

  meson install -C build --destdir "$pkgdir" "${_meson_install[@]}"

  # we'll create this on installation
  rmdir "$pkgdir"/var/log/journal/remote

  # runtime libraries shipped with systemd-libs
  install -d -m0755 systemd-libs/lib/
  mv "$pkgdir"/usr/lib/lib{nss,systemd,udev}*.so* systemd-libs/lib/
  mv "$pkgdir"/usr/lib/pkgconfig systemd-libs/lib/pkgconfig
  mv "$pkgdir"/usr/include systemd-libs/include
  mv "$pkgdir"/usr/share/man/man3 systemd-libs/man3

  # ukify shipped in separate package
  install -d -m0755 systemd-ukify/{bin,systemd,man1,install.d}
  mv "$pkgdir"/usr/bin/ukify systemd-ukify/bin/
  mv "$pkgdir"/usr/lib/systemd/ukify systemd-ukify/systemd/
  mv "$pkgdir"/usr/share/man/man1/ukify.1 systemd-ukify/man1/
  # we move the ukify hook itself, but keep 90-uki-copy.install in place,
  # because there are other ways to generate UKIs w/o ukify, e.g. w/ mkinitcpio
  mv "$pkgdir"/usr/lib/kernel/install.d/60-ukify.install systemd-ukify/install.d

  # manpages shipped with systemd-sysvcompat
  rm "$pkgdir"/usr/share/man/man8/{halt,poweroff,reboot,shutdown}.8

  # executable (symlinks) shipped with systemd-sysvcompat
  rm "$pkgdir"/usr/bin/{halt,init,poweroff,reboot,shutdown}

  # files shipped with systemd-resolvconf
  rm "$pkgdir"/usr/{bin/resolvconf,share/man/man1/resolvconf.1}

  # tests shipped with systemd-tests (for upstream)
  install -d -m0755 systemd-tests/
  mv "$pkgdir"/usr/lib/systemd/tests systemd-tests/

  # avoid a potential conflict with [core]/filesystem
  rm "$pkgdir"/usr/share/factory/etc/{issue,nsswitch.conf}
  sed -i -e '/^C \/etc\/nsswitch\.conf/d' \
    -e '/^C \/etc\/issue/d' "$pkgdir"/usr/lib/tmpfiles.d/etc.conf

  # ship default policy to leave services disabled
  echo 'disable *' >"$pkgdir"/usr/lib/systemd/system-preset/99-default.preset

  # The group 'systemd-journal' is allocated dynamically and may have varying
  # gid on different systems. Let's install with gid 0 (root), systemd-tmpfiles
  # will fix the permissions for us. (see /usr/lib/tmpfiles.d/systemd.conf)
  install -d -o root -g root -m 2755 "$pkgdir"/var/log/journal

  # add example bootctl configuration
  install -D -m0644 manjaro.conf "$pkgdir"/usr/share/systemd/bootctl/manjaro.conf
  install -D -m0644 loader.conf "$pkgdir"/usr/share/systemd/bootctl/loader.conf
  install -D -m0644 splash-manjaro.bmp "$pkgdir"/usr/share/systemd/bootctl/splash-manjaro.bmp

  # pacman hooks
  install -D -m0755 systemd-hook "$pkgdir"/usr/share/libalpm/scripts/systemd-hook
  install -D -m0644 -t "$pkgdir"/usr/share/libalpm/hooks *.hook

  # overwrite the systemd-user PAM configuration with our own
  install -D -m0644 systemd-user.pam "$pkgdir"/etc/pam.d/systemd-user

  # create a directory for cryptsetup keys
  install -d -m0700 "$pkgdir"/etc/cryptsetup-keys.d

  # handle uncommon license
  install -d -m0755 "$pkgdir/usr/share/licenses/$pkgbase"
  ln -s -t "$_" /usr/share/doc/systemd/LICENSES/MIT-0.txt
}

package_systemd-libs() {
  pkgdesc='systemd client libraries'
  depends=('glibc' 'gcc-libs' 'libcap' 'libgcrypt' 'lz4' 'xz' 'zstd')
  license+=(
    'CC0-1.0' # siphash
    'GPL-2.0-or-later WITH Linux-syscall-note' # src/basic/linux/*
  )
  provides=('libsystemd' 'libsystemd.so' 'libudev.so')
  conflicts=('libsystemd')
  replaces=('libsystemd')

  install -d -m0755 "$pkgdir"/usr/share/man
  mv systemd-libs/lib "$pkgdir"/usr/lib
  mv systemd-libs/include "$pkgdir"/usr/include
  mv systemd-libs/man3 "$pkgdir"/usr/share/man/man3
}

package_systemd-resolvconf() {
  pkgdesc='systemd resolvconf replacement (for use with systemd-resolved)'
  depends=("systemd=${pkgver}")
  provides=('openresolv' 'resolvconf')
  conflicts=('resolvconf')

  install -d -m0755 "$pkgdir"/usr/bin
  ln -s resolvectl "$pkgdir"/usr/bin/resolvconf

  install -d -m0755 "$pkgdir"/usr/share/man/man1
  ln -s resolvectl.1.gz "$pkgdir"/usr/share/man/man1/resolvconf.1.gz
}

package_systemd-sysvcompat() {
  pkgdesc='sysvinit compat for systemd'
  conflicts=('sysvinit')
  depends=("systemd=${pkgver}")

  install -D -m0644 -t "$pkgdir"/usr/share/man/man8 \
    build/man/{halt,poweroff,reboot,shutdown}.8

  install -d -m0755 "$pkgdir"/usr/bin
  ln -s ../lib/systemd/systemd "$pkgdir"/usr/bin/init
  for tool in halt poweroff reboot shutdown; do
    ln -s systemctl "$pkgdir"/usr/bin/$tool
  done
}

package_systemd-tests() {
  pkgdesc='systemd tests'
  depends=("systemd=${pkgver}")

  install -d -m0755 "$pkgdir"/usr/lib/systemd
  mv systemd-tests/tests "$pkgdir"/usr/lib/systemd/tests
}

package_systemd-ukify() {
  pkgdesc='Combine kernel and initrd into a signed Unified Kernel Image'
  provides=('ukify')
  depends=("systemd=${pkgver}" 'binutils' 'python-cryptography' 'python-pefile')
  optdepends=('python-pillow: Show the size of splash image'
              'sbsigntools: Sign the embedded kernel')

  install -d -m0755 "$pkgdir"/usr/{lib/kernel,share/man}
  mv systemd-ukify/bin "$pkgdir"/usr/bin
  mv systemd-ukify/systemd "$pkgdir"/usr/lib/systemd
  mv systemd-ukify/man1 "$pkgdir"/usr/share/man/man1
  mv systemd-ukify/install.d "$pkgdir"/usr/lib/kernel/install.d
}

# vim:ft=sh syn=sh et sw=2:


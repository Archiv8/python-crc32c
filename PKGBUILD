#!/bin/bash

# Based on the orginal packaging by Martino Pilia <martino.pilia@gmail.com>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# [ToDo]: Add files: User documentation
# [ToDo]: Add files: Tooling
# [FixMe]: Namcap warnings and errors

# Maintainer: Ross Clark <https://github.com/orgs/Archiv8/python-crc32c/discussions>
# Contributor: Ross Clark <https://github.com/orgs/Archiv8/python-crc32c/discussions>

_langname="python"
_relname="crc32c"

pkgname="${_langname}-${_relname}"
pkgver=2.2
pkgrel=1
pkgdesc="Implementation of the crc32c algorithm in hardware and software"
arch=(
	"any"
	)
url="https://github.com/ICRAR/crc32c"
license=(
	"LGPL2"
	)
depends=(
	# Arch Linux Official Repositories
	"python"
	)
makedepends=(
	# Arch Linux Official Repositories
	"python-setuptools"
	)
source+=(
	"https://github.com/ICRAR/crc32c/archive/v${pkgver}.tar.gz"
	)
sha512sums=(
	"b64b572215bd0b17e9f0d92cccfa2bcf57f2efd94642ef42e4fbb1a4ad5cbf2f6493dd8152d27aa340089c92d84940b11532bf573a9384907f2112e295500d68"
	)

package() {
	cd "${srcdir}/${_relname}-${pkgver}"
	python setup.py install --optimize=1 --root="${pkgdir}"
}

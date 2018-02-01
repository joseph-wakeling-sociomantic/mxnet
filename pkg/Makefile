DEB_PACKAGE_VERSION ?= $(shell git describe)

DEB_PACKAGE_ITERATION = $(shell echo $(DEB_PACKAGE_VERSION) | sed 's/.*-//')

PKGVERSION ?= $(shell echo $(DEB_PACKAGE_VERSION) | sed 's/-$(DEB_PACKAGE_ITERATION)//' | cut -c 2-)
PKGITERATION ?= $(DEB_PACKAGE_ITERATION)~$(shell lsb_release -cs)

include ../makd/Makd.mak

PKG_NAME = knock
PKG_EXT = tar.gz
PKG_DOWNLOAD_METHOD = git
PKG_GIT_HASH = 258a27e
PKG_DIST_SITE = https://github.com/jvinet/knock.git
PKG_DIST_FILE = $(PKG_NAME)-git$(PKG_GIT_HASH).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-git$(PKG_GIT_HASH)

DEPENDS = cross/libpcap

HOMEPAGE = http://www.zeroflux.org/projects/knock
COMMENT  = Uport-knock server.
LICENSE  = 

GNU_CONFIGURE = 1

CONFIGURE_ARGS = --prefix=$(STAGING_INSTALL_PREFIX)


PRE_CONFIGURE_TARGET = myPreConfigure

include ../../mk/spksrc.cross-cc.mk

.PHONY: myPreConfigure
myPreConfigure:
	$(RUN) autoreconf -i -f


include $(TOPDIR)/rules.mk

PKG_NAME:=perl-io-socket-ssl
PKG_VERSION:=2.073
PKG_RELEASE:=1

PKG_SOURCE:=IO-Socket-SSL-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/S/SU/SULLR/
PKG_HASH:=b2c0b34df97cb1aa816221cee2454a1efd89b86ccbda810389a30e0d08cf57c8

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=unknown

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/IO-Socket-SSL-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-io-socket-ssl
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=SSL sockets with IO::Socket interface
	URL:=https://metacpan.org/pod/IO::Socket::SSL/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar +perlbase-errno +perlbase-io +perl-net-ssleay
endef

define Package/perl-io-socket-ssl/description
	SSL sockets with IO::Socket interface.
	Note: Install perl-uri package if you need to verfify IDN with a certificate.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-io-socket-ssl/install
	$(call perlmod/Install,$(1),IO auto/IO)
endef

$(eval $(call BuildPackage,perl-io-socket-ssl))

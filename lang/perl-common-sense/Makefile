include $(TOPDIR)/rules.mk

PKG_NAME:=perl-common-sense
PKG_VERSION:=3.75
PKG_RELEASE:=1

PKG_SOURCE:=common-sense-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/M/ML/MLEHMANN/
PKG_HASH:=a86a1c4ca4f3006d7479064425a09fa5b6689e57261fcb994fe67d061cba0e7e

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=unknown

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/common-sense-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-common-sense
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=common::sense - save a tree AND a kitten
	URL:=https://metacpan.org/pod/distribution/common-sense/sense.pod
	DEPENDS:=perl +perlbase-essential
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-common-sense/install
	$(call perlmod/Install,$(1),common auto/common)
endef

$(eval $(call BuildPackage,perl-common-sense))

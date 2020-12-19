include $(TOPDIR)/rules.mk

PKG_NAME:=perl-cpanel-json-xs
PKG_VERSION:=4.25
PKG_RELEASE:=1

PKG_SOURCE:=Cpanel-JSON-XS-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/R/RU/RURBAN/
PKG_HASH:=f9ba3da53df92321fe73e7330692ba2e9758dc50e21f82f9cfc327e937202918

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=unknown

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Cpanel-JSON-XS-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-cpanel-json-xs
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=cPanel fork of JSON::XS, fast and correct serializing
	URL:=https://metacpan.org/pod/Cpanel::JSON::XS/
	DEPENDS:=perl +perlbase-essential +perlbase-encode +perlbase-xsloader +perlbase-attributes
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-cpanel-json-xs/install
	$(call perlmod/Install,$(1),Cpanel auto/Cpanel)
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bin/cpanel_json_xs $(1)/usr/bin
endef

$(eval $(call BuildPackage,perl-cpanel-json-xs))

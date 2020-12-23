include $(TOPDIR)/rules.mk

PKG_NAME:=perl-uri-nested
PKG_VERSION:=0.10
PKG_RELEASE:=1

PKG_SOURCE:=URI-Nested-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/D/DW/DWHEELER/
PKG_HASH:=e1971339a65fbac63ab87142d4b59d3d259d51417753c77cb58ea31a8233efaf

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/URI-Nested-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-uri-nested
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Nested URIs
	URL:=https://metacpan.org/pod/URI::Nested/
	DEPENDS:=perl +perlbase-essential +perl-uri
endef

define Package/perl-uri-nested/description
	URI::Nested - Nested URIs.
endef

define Build/Configure
endef

define Build/Compile
	$(INSTALL_DIR) $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(CP) $(PKG_BUILD_DIR)/lib/* $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type d -exec chmod 755 {} \;
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type f -exec chmod 644 {} \;
endef

define Package/perl-uri-nested/install
	$(call perlmod/Install,$(1),URI)
endef

$(eval $(call BuildPackage,perl-uri-nested))

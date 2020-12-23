include $(TOPDIR)/rules.mk

PKG_NAME:=perl-uri-db
PKG_VERSION:=0.19
PKG_RELEASE:=1

PKG_SOURCE:=URI-db-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/D/DW/DWHEELER/
PKG_HASH:=c4999deaf451652216032c8e327ff6e6d655539eac379095bb69b0c369efa658

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/URI-db-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-uri-db
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Database URIs
	URL:=https://metacpan.org/pod/URI::db/
	DEPENDS:=perl +perlbase-essential +perl-uri +perl-uri-nested
endef

define Package/perl-uri-db/description
	URI::db - Database URIs.
endef

define Build/Configure
endef

define Build/Compile
	$(INSTALL_DIR) $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(CP) $(PKG_BUILD_DIR)/lib/* $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type d -exec chmod 755 {} \;
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type f -exec chmod 644 {} \;
endef

define Package/perl-uri-db/install
	$(call perlmod/Install,$(1),URI)
endef

$(eval $(call BuildPackage,perl-uri-db))

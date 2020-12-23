include $(TOPDIR)/rules.mk

PKG_NAME:=perl-mojo-sqlite
PKG_VERSION:=3.004
PKG_RELEASE:=2

PKG_SOURCE:=Mojo-SQLite-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/D/DB/DBOOK/
PKG_HASH:=d9ca9c1f3e8183611638e318b88ad3c0f8ab7e65f6ac72e48bffe51aea03b983

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=Artistic-2.0

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Mojo-SQLite-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-mojo-sqlite
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=A tiny Mojolicious wrapper for SQLite
	URL:=https://metacpan.org/pod/Mojo::SQLite/
	DEPENDS:=perl +perlbase-essential +perl-dbd-sqlite +perl-dbi +perl-mojolicious +perlbase-scalar +perlbase-file +perl-uri-db +perl-uri
endef

define Package/perl-mojo-sqlite/description
	Mojo::SQLite - A tiny Mojolicious wrapper for SQLite.
endef

define Build/Configure
endef

define Build/Compile
	$(INSTALL_DIR) $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(CP) $(PKG_BUILD_DIR)/lib/* $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type d -exec chmod 755 {} \;
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type f -exec chmod 644 {} \;
endef

define Package/perl-mojo-sqlite/install
	$(call perlmod/Install,$(1),Mojo)
endef

$(eval $(call BuildPackage,perl-mojo-sqlite))

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-minion-backend-sqlite
PKG_VERSION:=5.0.3
PKG_RELEASE:=1

PKG_SOURCE:=Minion-Backend-SQLite-v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/D/DB/DBOOK/
PKG_HASH:=64c55e0be0ff457a3295e04537548098e48469972c526b7cd0213f66081209b2

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=artistic_2

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Minion-Backend-SQLite-v$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-minion-backend-sqlite
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=SQLite backend for Minion job queue
	URL:=https://metacpan.org/pod/Minion::Backend::SQLite/
	DEPENDS:=perl +perlbase-essential +perl-mojolicious +perl-minion +perl-mojo-sqlite +perlbase-list +perlbase-sys +perlbase-time
endef

define Package/perl-minion-backend-sqlite/description
	Minion::Backend::SQLite - SQLite backend for Minion job queue.
endef

define Build/Configure
endef

define Build/Compile
	$(INSTALL_DIR) $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(CP) $(PKG_BUILD_DIR)/lib/* $(PKG_INSTALL_DIR)$(PERL_SITELIB)
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type d -exec chmod 755 {} \;
	$(FIND) $(PKG_INSTALL_DIR)$(PERL_SITELIB) -type f -exec chmod 644 {} \;
endef

define Package/perl-minion-backend-sqlite/install
	$(call perlmod/Install,$(1),Minion)
endef

$(eval $(call BuildPackage,perl-minion-backend-sqlite))

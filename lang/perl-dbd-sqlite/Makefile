include $(TOPDIR)/rules.mk

PKG_NAME:=perl-dbd-sqlite
PKG_VERSION:=1.66
PKG_RELEASE:=1

PKG_SOURCE:=DBD-SQLite-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/I/IS/ISHIGAKI/
PKG_HASH:=89e75dff9f66c273e0e459d51f151f88960eb7d82e2821e6902f18688ba592fe

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/DBD-SQLite-$(PKG_VERSION)

PKG_BUILD_DEPENDS:=perl-dbi/host

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-dbd-sqlite
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=DBD::SQLite - Self-contained RDBMS
	URL:=https://metacpan.org/pod/DBD::SQLite/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar +perlbase-dynaloader +perlbase-xsloader +perl-dbi
endef

define Package/perl-dbd-sqlite/description
	DBD::SQLite - Self-contained RDBMS in a DBI driver.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-dbd-sqlite/install
	$(call perlmod/Install,$(1),DBD auto/DBD)
endef

$(eval $(call BuildPackage,perl-dbd-sqlite))

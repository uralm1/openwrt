include $(TOPDIR)/rules.mk

PKG_NAME:=perl-sql-abstract
PKG_VERSION:=1.87
PKG_RELEASE:=1

PKG_SOURCE:=SQL-Abstract-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/I/IL/ILMARI/
PKG_HASH:=e926a0a83da7efa18e57e5b2952a2ab3b7563a51733fc6dd5c89f12156481c4a

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/SQL-Abstract-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-sql-abstract
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Generate SQL from Perl data structures
	URL:=https://metacpan.org/pod/SQL::Abstract/
	DEPENDS:=perl +perlbase-essential +perlbase-list +perlbase-scalar +perlbase-mro +perlbase-text
endef

define Package/perl-sql-abstract/description
	SQL::Abstract - Generate SQL from Perl data structures.
	Note: SQL::Abstract::Tree requires Moo,Sub::Quote,Hash::Merge modules that
	don't included in DEPENDS. Install them if needed.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-sql-abstract/install
	$(call perlmod/Install,$(1),SQL auto/SQL DBIx)
endef

$(eval $(call BuildPackage,perl-sql-abstract))

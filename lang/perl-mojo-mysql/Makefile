include $(TOPDIR)/rules.mk

PKG_NAME:=perl-mojo-mysql
PKG_VERSION:=1.22
PKG_RELEASE:=1

PKG_SOURCE:=Mojo-mysql-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/J/JH/JHTHORSEN/
PKG_HASH:=905a06e0fffd030be6e20bb79d24fe5b7b53bcce64eb7985f1aa5076130e6006

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=Artistic-2.0

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Mojo-mysql-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-mojo-mysql
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Mojolicious and Async MySQL/MariaDB
	URL:=https://metacpan.org/pod/Mojo::mysql/
	DEPENDS:=perl +perlbase-essential +perl-dbd-mysql +perl-dbi +perl-mojolicious +perl-sql-abstract
endef

define Package/perl-mojo-mysql/description
	Mojo::mysql - Mojolicious and Async MySQL/MariaDB.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-mojo-mysql/install
	$(call perlmod/Install,$(1),Mojo auto/Mojo SQL)
endef

$(eval $(call BuildPackage,perl-mojo-mysql))

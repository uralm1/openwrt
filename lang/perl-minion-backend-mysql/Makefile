include $(TOPDIR)/rules.mk

PKG_NAME:=perl-minion-backend-mysql
PKG_VERSION:=0.23
PKG_RELEASE:=1

PKG_SOURCE:=Minion-Backend-mysql-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/P/PR/PREACTION/
PKG_HASH:=3ddaf2b038d42d19387c306ac2381d6d748a5619cc3c25c7525f196cd904f821

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Minion-Backend-mysql-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-minion-backend-mysql
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Minion::Backend::mysql
	URL:=https://metacpan.org/pod/Minion::Backend::mysql/
	DEPENDS:=perl +perlbase-essential +perl-mojolicious +perl-minion +perl-mojo-mysql +perlbase-sys +perlbase-time
endef

define Package/perl-minion-backend-mysql/description
	Minion::Backend::mysql - Mysql backend for Minion job queue.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-minion-backend-mysql/install
	$(call perlmod/Install,$(1),Minion auto/Minion)
endef

$(eval $(call BuildPackage,perl-minion-backend-mysql))

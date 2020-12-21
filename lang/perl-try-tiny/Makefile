include $(TOPDIR)/rules.mk

PKG_NAME:=perl-try-tiny
PKG_VERSION:=0.30
PKG_RELEASE:=1

PKG_SOURCE:=Try-Tiny-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/E/ET/ETHER/
PKG_HASH:=da5bd0d5c903519bbf10bb9ba0cb7bcac0563882bcfe4503aee3fb143eddef6b

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=mit

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Try-Tiny-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-try-tiny
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Minimal try/catch with proper preservation of $$@
	URL:=https://metacpan.org/pod/Try::Tiny/
	DEPENDS:=perl +perlbase-essential
endef

define Package/perl-try-tiny/description
	Try::Tiny - Minimal try/catch with proper preservation of $$@.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-try-tiny/install
	$(call perlmod/Install,$(1),Try auto/Try)
endef

$(eval $(call BuildPackage,perl-try-tiny))

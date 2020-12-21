include $(TOPDIR)/rules.mk

PKG_NAME:=perl-clone
PKG_VERSION:=0.45
PKG_RELEASE:=1

PKG_SOURCE:=Clone-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/A/AT/ATOOMIC/
PKG_HASH:=cbb6ee348afa95432e4878893b46752549e70dc68fe6d9e430d1d2e99079a9e6

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Clone-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-clone
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Recursively copy Perl datatypes
	URL:=https://metacpan.org/pod/Clone/
	DEPENDS:=perl +perlbase-essential +perlbase-xsloader +perlbase-dynaloader +perlbase-autoloader
endef

define Package/perl-clone/description
	Clone - Recursively copy Perl datatypes.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-clone/install
	$(call perlmod/Install,$(1),Clone.pm auto/Clone)
endef

$(eval $(call BuildPackage,perl-clone))

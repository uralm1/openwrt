include $(TOPDIR)/rules.mk

PKG_NAME:=perl-moo
PKG_VERSION:=2.004004
PKG_RELEASE:=1

PKG_SOURCE:=Moo-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/H/HA/HAARG/
PKG_HASH:=714b77b115788708c6d8ab6f18eea173f8109d397aecd34e32cc71a0ffcf2246

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Moo-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-moo
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Minimalist Object Orientation
	URL:=https://metacpan.org/pod/Moo/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar +perl-role-tiny +perl-sub-quote +perl-sub-defer
endef

define Package/perl-moo/description
	Moo - Minimalist Object Orientation (with Moose compatibility).
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-moo/install
	$(call perlmod/Install,$(1),Moo auto/Moo Moo.pm oo.pm Method)
endef

$(eval $(call BuildPackage,perl-moo))

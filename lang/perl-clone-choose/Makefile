include $(TOPDIR)/rules.mk

PKG_NAME:=perl-clone-choose
PKG_VERSION:=0.010
PKG_RELEASE:=1

PKG_SOURCE:=Clone-Choose-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/H/HE/HERMES/
PKG_HASH:=5623481f58cee8edb96cd202aad0df5622d427e5f748b253851dfd62e5123632

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Clone-Choose-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-clone-choose
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Choose appropriate clone utility
	URL:=https://metacpan.org/pod/Clone::Choose/
	DEPENDS:=perl +perlbase-essential
endef

define Package/perl-clone-choose/description
	Close::Choose - Choose appropriate clone utility.
	Install one of perl-clone(better) or perlbase-storable package to choose from.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-clone-choose/install
	$(call perlmod/Install,$(1),Clone auto/Clone)
endef

$(eval $(call BuildPackage,perl-clone-choose))

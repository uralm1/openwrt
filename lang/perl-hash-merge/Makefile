include $(TOPDIR)/rules.mk

PKG_NAME:=perl-hash-merge
PKG_VERSION:=0.302
PKG_RELEASE:=1

PKG_SOURCE:=Hash-Merge-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/H/HE/HERMES/
PKG_HASH:=ae0522f76539608b61dde14670e79677e0f391036832f70a21f31adde2538644

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Hash-Merge-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-hash-merge
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Merges arbitrarily deep hashes into a single hash
	URL:=https://metacpan.org/pod/Hash::Merge/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar +perl-clone-choose
endef

define Package/perl-hash-merge/description
	Hash::Merge - Merges arbitrarily deep hashes into a single hash.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-hash-merge/install
	$(call perlmod/Install,$(1),Hash auto/Hash)
endef

$(eval $(call BuildPackage,perl-hash-merge))

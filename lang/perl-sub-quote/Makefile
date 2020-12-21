include $(TOPDIR)/rules.mk

PKG_NAME:=perl-sub-quote
PKG_VERSION:=2.006006
PKG_RELEASE:=1

PKG_SOURCE:=Sub-Quote-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/H/HA/HAARG/
PKG_HASH:=6e4e2af42388fa6d2609e0e82417de7cc6be47223f576592c656c73c7524d89d

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Sub-Quote-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-sub-quote
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Efficient generation of subroutines via string eval
	URL:=https://metacpan.org/pod/Sub::Quote/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar
endef

define Package/perl-sub-quote/description
	Sub::Quote - Efficient generation of subroutines via string eval.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-sub-quote/install
	$(call perlmod/Install,$(1),Sub/Quote.pm auto/Sub/Quote)
endef

$(eval $(call BuildPackage,perl-sub-quote))


define Package/perl-sub-defer
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Defer generation of subroutines until tey are first called
	URL:=https://metacpan.org/pod/Sub::Defer/
	DEPENDS:=perl +perlbase-essential +perlbase-scalar
endef

define Package/perl-sub-defer/description
	Sub::Defer - Defer generation of subroutines until tey are first called.
endef

define Package/perl-sub-defer/install
	$(call perlmod/Install,$(1),Sub/Defer.pm)
endef

$(eval $(call BuildPackage,perl-sub-defer))

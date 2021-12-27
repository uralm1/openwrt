include $(TOPDIR)/rules.mk

PKG_NAME:=perl-ev
PKG_VERSION:=4.33
PKG_RELEASE:=2

PKG_SOURCE:=EV-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/M/ML/MLEHMANN/
PKG_HASH:=4aee8391b88113b42187f91fd49245fdc8e9b193a15ac202f519caae2aa8ea35

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=unknown

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/EV-$(PKG_VERSION)

PKG_BUILD_DEPENDS:=perl-canary-stability/host

PKG_USE_MIPS16:=0

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-ev
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Perl interface to libev, a high perfomance event loop
	URL:=https://metacpan.org/pod/EV/
	DEPENDS:=perl +perlbase-essential +perlbase-xsloader +perl-common-sense
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-ev/install
	$(call perlmod/Install,$(1),EV EV.pm auto/EV)
endef

$(eval $(call BuildPackage,perl-ev))

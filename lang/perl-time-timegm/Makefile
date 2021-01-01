include $(TOPDIR)/rules.mk

PKG_NAME:=perl-time-timegm
PKG_VERSION:=0.01
PKG_RELEASE:=1

PKG_SOURCE:=Time-timegm-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/P/PE/PEVANS/
PKG_HASH:=e721cdfda183146b895e04cee712e10ab1bc73c8bad1bbc84c04b19ef1052c98

PKG_MAINTAINER:=Ural Khasanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Time-timegm-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-time-timegm
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=A UTC version of mktime()
	URL:=https://metacpan.org/pod/Time::timegm/
	DEPENDS:=perl +perlbase-essential +perlbase-posix +perlbase-xsloader
endef

define Package/perl-time-timegm/description
	Time::timegm - A UTC version of mktime().
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-time-timegm/install
	$(call perlmod/Install,$(1),Time auto/Time)
endef

$(eval $(call BuildPackage,perl-time-timegm))

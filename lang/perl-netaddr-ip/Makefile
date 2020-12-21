include $(TOPDIR)/rules.mk

PKG_NAME:=perl-netaddr-ip
PKG_VERSION:=4.079
PKG_RELEASE:=2

PKG_SOURCE_URL:=http://www.cpan.org/authors/id/M/MI/MIKER/
PKG_SOURCE:=NetAddr-IP-$(PKG_VERSION).tar.gz
PKG_HASH:=ec5a82dfb7028bcd28bb3d569f95d87dd4166cc19867f2184ed3a59f6d6ca0e7

PKG_LICENSE:=GPL-1.0-or-later Artistic-1.0-Perl
PKG_MAINTAINER:=Ural Khassanov <uralm1@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/NetAddr-IP-$(PKG_VERSION)

#PKG_BUILD_DEPENDS:=perl

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-netaddr-ip
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Manages IPv4 and IPv6 addresses and subnets
  URL:=https://metacpan.org/pod/NetAddr::IP
  DEPENDS:=perl +perlbase-essential +perlbase-autoloader +perlbase-storable +perlbase-dynaloader
endef

define Package/perl-netaddr-ip/description
	NetAddr::IP manages IPv4 and IPv6 addresses and subnets.
endef

define Build/Configure
	$(call perlmod/Configure,,)
	$(call perlmod/Configure,,,"$(PKG_BUILD_DIR)/Lite")
	$(call perlmod/Configure,,,"$(PKG_BUILD_DIR)/Lite/Util")
endef

define Build/Compile
	$(call perlmod/Compile,,)
	$(call perlmod/Compile,,,"$(PKG_BUILD_DIR)/Lite")
	$(call perlmod/Compile,,,"$(PKG_BUILD_DIR)/Lite/Util")
endef

define Package/perl-netaddr-ip/install
	$(call perlmod/Install,$(1),NetAddr auto/NetAddr)
endef


$(eval $(call BuildPackage,perl-netaddr-ip))

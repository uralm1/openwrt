include $(TOPDIR)/rules.mk

PKG_NAME:=perl-net-ssleay
PKG_VERSION:=1.90
PKG_RELEASE:=1

PKG_SOURCE:=Net-SSLeay-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/C/CH/CHRISN/
PKG_HASH:=f8696cfaca98234679efeedc288a9398fcf77176f1f515dbc589ada7c650dc93

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=Artistic-2.0

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Net-SSLeay-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-net-ssleay
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Perl bindings for libssl and libcrypto
	URL:=https://metacpan.org/pod/Net::SSLeay/
	DEPENDS:=perl +perlbase-essential +perlbase-mime +perlbase-socket +perlbase-errno +perlbase-xsloader +perlbase-autoloader +libopenssl +zlib
endef

# for some strange reason in openwrt-21.02 perl makemaker receives INC="/usr/include"
# this results to build errors...
define Build/Configure
	$(call perlmod/Configure,,PERL_MM_OPT='INC=""')
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-net-ssleay/install
	$(call perlmod/Install,$(1),Net auto/Net)
endef

$(eval $(call BuildPackage,perl-net-ssleay))

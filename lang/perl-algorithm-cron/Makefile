include $(TOPDIR)/rules.mk

PKG_NAME:=perl-algorithm-cron
PKG_VERSION:=0.10
PKG_RELEASE:=1

PKG_SOURCE:=Algorithm-Cron-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/P/PE/PEVANS/
PKG_HASH:=adbc89ffbb758259e8ed18a9b99308ec853cac2f828a7c6530ce636d1056de3b

PKG_MAINTAINER:=Ural Khasanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Algorithm-Cron-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-algorithm-cron
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Implementation of the cron(8) scheduling algorithm
	URL:=https://metacpan.org/pod/Algorithm::Cron/
	DEPENDS:=perl +perlbase-essential +perlbase-posix +perl-time-timegm
endef

define Package/perl-algorithm-cron/description
	Algorithm::Cron - Abstract implementation of the cron(8) scheduling algorithm.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-algorithm-cron/install
	$(call perlmod/Install,$(1),Algorithm auto/Algorithm)
endef

$(eval $(call BuildPackage,perl-algorithm-cron))

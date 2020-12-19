include $(TOPDIR)/rules.mk

PKG_NAME:=perl-canary-stability
PKG_VERSION:=2013
PKG_RELEASE:=1

PKG_SOURCE:=Canary-Stability-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/M/ML/MLEHMANN/
PKG_HASH:=a5c91c62cf95fcb868f60eab5c832908f6905221013fea2bce3ff57046d7b6ea

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=unknown

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Canary-Stability-$(PKG_VERSION)
HOST_BUILD_DIR:=$(BUILD_DIR_HOST)/perl/Canary-Stability-$(PKG_VERSION)

HOST_BUILD_DEPENDS:=perl/host

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-canary-stability
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Canary to check perl compatibility
	URL:=https://metacpan.org/pod/Canary::Stability/
	DEPENDS:=perl +perlbase-essential
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Host/Configure
	$(call perlmod/host/Configure,,)
endef

define Host/Compile
	$(call perlmod/host/Compile,,)
endef

define Host/Install
	$(call perlmod/host/Install,$(1),)
endef

define Package/perl-canary-stability/install
	$(call perlmod/Install,$(1),Canary auto/Canary)
endef

$(eval $(call BuildPackage,perl-canary-stability))
$(eval $(call HostBuild))

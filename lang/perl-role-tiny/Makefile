include $(TOPDIR)/rules.mk

PKG_NAME:=perl-role-tiny
PKG_VERSION:=2.001004
PKG_RELEASE:=1

PKG_SOURCE:=Role-Tiny-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/H/HA/HAARG/
PKG_HASH:=92ba5712850a74102c93c942eb6e7f62f7a4f8f483734ed289d08b324c281687

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=perl_5

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Role-Tiny-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-role-tiny
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Roles: a nouvelle cuisine portion size slice of Moose
	URL:=https://metacpan.org/pod/Role::Tiny/
	DEPENDS:=perl +perlbase-essential +perlbase-mro
endef

define Package/perl-role-tiny/description
	Role::Tiny - Roles: a nouvelle cuisine portion size slice of Moose.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-role-tiny/install
	$(call perlmod/Install,$(1),Role auto/Role)
endef

$(eval $(call BuildPackage,perl-role-tiny))

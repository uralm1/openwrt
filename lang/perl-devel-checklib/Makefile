include $(TOPDIR)/rules.mk

PKG_NAME:=perl-devel-checklib
PKG_VERSION:=1.14
PKG_RELEASE:=1

PKG_SOURCE_URL:=http://www.cpan.org/authors/id/M/MA/MATTN/
PKG_SOURCE:=Devel-CheckLib-$(PKG_VERSION).tar.gz
PKG_HASH:=f21c5e299ad3ce0fdc0cb0f41378dca85a70e8d6c9a7599f0e56a957200ec294

PKG_LICENSE:=GPL-1.0-or-later Artistic-1.0-Perl
PKG_MAINTAINER:=Ural Khassanov <uralm1@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Devel-CheckLib-$(PKG_VERSION)
HOST_BUILD_DIR:=$(BUILD_DIR_HOST)/perl/Devel-CheckLib-$(PKG_VERSION)

HOST_BUILD_DEPENDS:=perl/host

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-devel-checklib
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Devel::CheckLib check that library is available
  URL:=https://metacpan.org/pod/Devel::CheckLib
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

define Package/perl-devel-checklib/install
	$(call perlmod/Install,$(1),Devel auto/Devel)
endef


$(eval $(call BuildPackage,perl-devel-checklib))
$(eval $(call HostBuild))

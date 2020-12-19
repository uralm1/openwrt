include $(TOPDIR)/rules.mk

PKG_NAME:=perl-sys-runalone
PKG_VERSION:=0.13
PKG_RELEASE:=1

PKG_SOURCE_URL:=http://www.cpan.org/authors/id/T/TI/TILLY/
PKG_SOURCE:=Sys-RunAlone-$(PKG_VERSION).tar.gz
PKG_HASH:=b5492d7f267fb116e604022eaf5bda191f7adb9ee85e35340e75ef86acb48822

PKG_LICENSE:=GPL-1.0-or-later Artistic-1.0-Perl
PKG_MAINTAINER:=Ural Khassanov <uralm1@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Sys-RunAlone-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-sys-runalone
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Sys::RunAlone makes sure only one invocation is active
  URL:=https://metacpan.org/pod/Sys::RunAlone
  DEPENDS:=perl +perlbase-essential +perlbase-fcntl
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-sys-runalone/install
	$(call perlmod/Install,$(1),Sys auto/Sys)
endef


$(eval $(call BuildPackage,perl-sys-runalone))

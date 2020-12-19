include $(TOPDIR)/rules.mk

PKG_NAME:=perl-dbd-mysql
PKG_VERSION:=4.050
PKG_RELEASE:=1

PKG_SOURCE_URL:=http://www.cpan.org/authors/id/D/DV/DVEEDEN/
PKG_SOURCE:=DBD-mysql-$(PKG_VERSION).tar.gz
PKG_HASH:=4f48541ff15a0a7405f76adc10f81627c33996fbf56c95c26c094444c0928d78

PKG_LICENSE:=GPL-1.0-or-later Artistic-1.0-Perl
PKG_MAINTAINER:=Ural Khassanov <uralm1@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/DBD-mysql-$(PKG_VERSION)

PKG_BUILD_DEPENDS:=perl-devel-checklib/host perl-dbi/host

#PKG_LEAVE_COMMENTS:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-dbd-mysql
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Perl DBI driver for the MySQL database
  URL:=https://metacpan.org/pod/DBD::mysql
  DEPENDS:=perl +perlbase-essential +perl-dbi +libmysqlclient +libopenssl +zlib $(ICONV_DEPENDS)
endef

#define Build/Prepare
#	$(Build/Prepare/Default)
#endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-dbd-mysql/install
	$(call perlmod/Install,$(1),Bundle DBD auto/DBD)
endef


$(eval $(call BuildPackage,perl-dbd-mysql))

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-mojolicious
PKG_VERSION:=8.67
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/S/SR/SRI/
PKG_SOURCE:=Mojolicious-$(PKG_VERSION).tar.gz
PKG_HASH:=bba0d6020d4f2a71fa0454d53f57997e18f1831559e670f1f195fdbb9d962a2c

PKG_LICENSE:=Artistic-2.0-Perl
PKG_MAINTAINER:=Ural Khassanov <uralm1@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Mojolicious-$(PKG_VERSION)

#PKG_BUILD_DEPENDS:=perl

PKG_LEAVE_COMMENTS:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-mojolicious
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Mojolicious - Real-time web framework
	URL:=https://metacpan.org/pod/Mojolicious
	DEPENDS:=perl +perlbase-essential +perlbase-io +perlbase-json-pp +perlbase-list +perlbase-hash +perlbase-file +perlbase-fcntl +perlbase-scalar +perlbase-time +perlbase-config +perlbase-posix +perlbase-encode +perlbase-pod +perlbase-symbol +perlbase-digest +perlbase-getopt +perlbase-mime +perlbase-unicode +perlbase-re +perlbase-cpan +perlbase-storable +perlbase-compress +perlbase-mro +perlbase-perlio +perlbase-utf8 +perlbase-cwd +perlbase-experimental
endef

define Package/perl-mojolicious/description
	Mojolicious - Real-time web framework
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

define Package/perl-mojolicious/install
	$(call perlmod/Install,$(1),Mojolicious auto/Mojolicious Mojolicious.pm Mojo Mojo.pm ojo.pm Test)
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/script/* $(1)/usr/bin
endef

$(eval $(call BuildPackage,perl-mojolicious))

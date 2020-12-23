include $(TOPDIR)/rules.mk

PKG_NAME:=perl-minion
PKG_VERSION:=10.14
PKG_RELEASE:=2

PKG_SOURCE:=Minion-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/S/SR/SRI/
PKG_HASH:=6f55d5cddc6271cd917b3232d6aef1ae7f0a48648e3c4539fe180b7283f940f7

PKG_MAINTAINER:=Ural Khassanov <uralm@uwc.ufanet.ru>
PKG_LICENSE:=Artistic-2.0

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Minion-$(PKG_VERSION)

PKG_LEAVE_COMMENTS:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/perl/perlmod.mk

define Package/perl-minion
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Minion - Job queue
	URL:=https://metacpan.org/pod/Minion/
	DEPENDS:=perl +perlbase-essential +perlbase-posix +perlbase-sys +perl-mojolicious
endef

define Package/perl-minion/description
	Minion - Job queue for Mojolicious.
	For Admin UI install perl-minion-admin package.
endef

define Build/Configure
	$(call perlmod/Configure,,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-minion/install
	$(call perlmod/Install,$(1),Minion auto/Minion Minion.pm Mojolicious/Plugin/Minion.pm)
endef

$(eval $(call BuildPackage,perl-minion))


define Package/perl-minion-admin
	SUBMENU:=Perl
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=Minion - Admin UI plugin
	URL:=https://metacpan.org/pod/Minion/
	DEPENDS:=perl +perlbase-essential +perl-minion
endef

define Package/perl-minion-admin/description
	Minion - AdminUI plugin (Mojolicious::Plugin::Minion::Admin).
endef

define Package/perl-minion-admin/install
	$(call perlmod/Install,$(1),Mojolicious/Plugin/Minion)
endef

$(eval $(call BuildPackage,perl-minion-admin))

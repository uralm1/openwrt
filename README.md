# OpenWrt uralm1 feed (perl packages for OpenWrt)
Mojolicious, Minion, etc...

```
# add to feeds.conf
src-link uralm1 /home/sv/src/openwrt/uralm1

# uninstall old perl-dbi, this feed provides new latest perl-dbi
# not needed in openwrt-21.02
#scripts/feeds uninstall perl-dbi

# install
scripts/feeds update uralm1
scripts/feeds install -a -p uralm1
```

Not needed in openwrt-21.02 (already upstream)
- perl-dbi
- perl-try-tiny
- perl-netaddr-ip

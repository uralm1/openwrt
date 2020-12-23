# OpenWrt uralm1 feed

```
# add to feeds.conf
src-link uralm1 /home/sv/src/openwrt/uralm1

# uninstall old perl-dbi, this feed provides new latest perl-dbi
scripts/feeds uninstall perl-dbi

# install
scripts/feeds update uralm1
scripts/feeds install -a -p uralm1
```

# [Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt) for newifi d2 (newifi 3)

源: [OpenWrt-19.07](https://github.com/openwrt/openwrt/tree/openwrt-19.07) (官方)

在[OpenWrt 官方 19.07.3 mt7621 配置选项 .config](https://downloads.openwrt.org/releases/19.07.3/targets/ramips/mt7621/config.buildinfo)基础上增加编译到固件里的内容：

* kmod-mt7603, kmod-mt76x2, wpad-basic, iwinfo 等无线相关。
* ca-certificates, ca-bundle, luci-compat, luci-app-upnp, luci-app-wol, dnsmasq-full (替代OP默认的 dnsmasq 包)
* blockd, usbutils, kmod-usb2, kmod-usb2-pci, kmod-usb3, kmod-usb-storage (usb设备挂载及相关内核模块)
* kmod-nls-iso8859-1, kmod-nls-cp932, kmod-nls-cp936, kmod-nls-cp950, kmod-nls-utf8 (kernel 的拉丁字符集, 日文, 简体中文, 繁体中文, utf8支持))
* curl, unzip, ipset, ip-full, bash, coreutils-nohup
* kmod-ipt-ipset, kmod-ipt-nat6, kmod-ipt-tproxy, kmod-tcp-bbr, kmod-tun, kmod-wireguard, iptables-mod-tproxy, ip6tables-mod-nat (网络相关内核模块)
* kmod-fs-ext4, kmod-fuse
* 其它启用的选项：CONFIG_KERNEL_FS_POSIX_ACL, CONFIG_KERNEL_USER_NS

打包进固件里的基准是可以直接装 luci-app-openclash 和 smartdns 。

测试 fuse 可用（rclone mount)。


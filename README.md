该版本fork于官方openwrt，略作修改，筛选稳定内核，以解决小米cr660x无故重启问题，仅针对660系列设置，其他设备不建议尝试！！！



![OpenWrt logo](include/logo.png)


OpenWrt Project 是一个针对嵌入式设备的 Linux 操作系统。OpenWrt 并没有尝试创建一个单一的静态固件，而是提供了一个具有包管理功能的完全可写文件系统。这将您从供应商提供的应用程序选择和配置中解放出来，并允许您通过使用包来定制设备以适应任何应用程序。对于开发人员来说，OpenWrt 是构建应用程序的框架，无需围绕它构建完整的固件；对于用户来说，这意味着完全定制的能力，以前所未有的方式使用设备。

Sunshine!

## 开发

要构建您自己的固件，您需要 GNU/Linux、BSD 或 MacOSX 系统（需要区分大小写的文件系统）。由于缺少区分大小写的文件系统，Cygwin 不受支持。

### 依赖

您需要以下工具来编译 OpenWrt，包名称因发行版而异。在[Build System Setup](https://openwrt.org/docs/guide-developer/build-system/install-buildsystem)文档中可以找到包含特定于发行版的软件包的完整列表 。

```
binutils bzip2 diff find flex gawk gcc-6+ getopt grep install libc-dev libz-dev
make4.1+ perl python3.6+ rsync subversion unzip which
```

### 快速上手

1. 运行./scripts/feeds update -a以获取 feeds.conf / feeds.conf.default 中定义的所有最新包定义

2. 运行./scripts/feeds install -a以将所有获得的包的符号链接安装到 package/feeds/

3. 运行make menuconfig以选择工具链、目标系统和固件包的首选配置。

4. 运行make以构建您的固件。这将下载所有源代码，构建交叉编译工具链，然后为您的目标系统交叉编译 GNU/Linux 内核和所有选定的应用程序。

### 相关资料库

主仓库使用多个子仓库来管理不同类别的包。所有包都通过名为opkg. 如果您正在寻找开发 OpenWrt 的 Web 界面或端口包，请在下面找到合适的存储库。

LuCI Web 界面：通过网络浏览器控制设备的现代模块化界面。

OpenWrt Packages：移植包的社区存储库。

OpenWrt Routing：专门针对（网状）路由的软件包。

## 支持信息

有关受支持设备的列表，请参阅 [OpenWrt 硬件数据库](https://openwrt.org/supported_devices)

### 文档

* [快速入门指南](https://openwrt.org/docs/guide-quick-start/start)
* [用户指南](https://openwrt.org/docs/guide-user/start)
* [开发者文档](https://openwrt.org/docs/guide-developer/start)
* [技术参考](https://openwrt.org/docs/techref/start)

### 支持社区

* [论坛](https://forum.openwrt.org): 用于使用、项目、讨论和硬件建议。
* [支持聊天](https://webchat.oftc.net/#openwrt): Channel `#openwrt` on **oftc.net**.

### 开发者社区

* [错误报告](https://bugs.openwrt.org): Report bugs in OpenWrt
* [开发邮件列表](https://lists.openwrt.org/mailman/listinfo/openwrt-devel): Send patches
* [Dev Chat](https://webchat.oftc.net/#openwrt-devel): Channel `#openwrt-devel` on **oftc.net**.

## 许可

OpenWrt 在 GPL-2.0 下获得许可

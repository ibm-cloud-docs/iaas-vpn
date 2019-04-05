---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 连接到 SSL VPN – MAC OSX 10x 和更高版本
{:#connect-ssl-vpn-mac-osx}

从 Apple Store 安装最新版本的 Mac MotionPro 客户机 v1.1.7。在更新之前，请确保卸载任何先前版本。

安装新客户机后，转至以下目录并使用终端应用程序启动 VPN。 

`/usr/local/motionpro/`

在其中，运行以下命令以连接到 SSL VPN：

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

可在[此处](https://www.softlayer.com/vpn-access)找到 VPN 端点列表。

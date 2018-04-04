---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 使用 SSL VPN

1. 在客户门户网站中通过从“导航”菜单中选择**支持 > SSL VPN 登录**以浏览至 **SSL VPN 登录**链接，然后输入您的凭证。
2. 在任务栏中看到“A”时，说明已建立 SSL VPN 隧道。
3. 恭喜您 - 您现在已接入专用 VLAN 中。

## 现在我已建立连接...接下来该如何做？

1. 使用 SSH 或 RDC（终端服务）连接到服务器的专用 IP 地址 (10.x.x.x) 以进行服务器管理。
2. 要利用远程控制台或重新引导功能，请通过 SuperMicro 软件（有关下载指示信息，请参阅[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/)）连接到 IPMI 2.0 卡。
3. 可以将驱动器映射到服务器 (Windows) 或将驱动器安装到服务器 (Red Hat)。

## 提示和技巧

1. IPMI IP 和专用 IP 之间只差一个数字 - 不要混淆这两个 IP。
2. 不能使用 SSH 或 RDC 来连接到 IPMI 卡，您必须使用相应软件。
3. 可以在每个**服务器**下的“硬件”部分中找到 IPMI IP 和专用 IP。
4. IPMI 卡会“侦听”专用 IP 接口，并将 IPMI 流量重定向到 IPMI 卡。

**警告：**

如果禁用 `eth0`（专用网络接口），那么将失去所有 IPMI 功能，包括监视、远程控制台和远程重新引导等。如果要锁定对专用接口的访问，请参阅可以在“IP 表”或“服务器防火墙”中输入的允许的 IP 地址列表。

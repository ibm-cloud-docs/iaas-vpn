---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 关于 VPN

通过 VPN 访问，您可以使用 IBM Cloud 专用网络来远程管理与帐户关联的所有服务器和服务。通过建立从您的位置到专用网络的 VPN 连接，便可以使用加密的 VPN 隧道进行带外管理和服务器急救。

使用专用网络进行通信本身就更安全。您可借此灵活地限制公共访问，同时仍然能够管理服务器。可向您帐户上的任何用户授予 VPN 访问权（以 SSL 和 PPTP 形式提供）。通过[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 进行的 VPN 交互支持在用户级别定制 VPN 访问权。

## 可通过哪些方式使用 SSL VPN？

使用此带外安全网关，您可以通过专用网络访问服务器。常见用途包括：

* 连接到服务器的专用 IP 地址 (10.x.x.x)（对于 SSH 或 RDC）。
* 连接到 IPMI 卡以进行远程控制台/访问/监视。
* 在家庭或工作 PC 的 Windows 或 Red Hat 中安装驱动器以方便使用。
* 关闭数据库服务器上的公共接口，并通过专用网络进行管理。
* 在第一次设置服务器时关闭公共接口。
* 在关键安全更新期间关闭公共接口。
* 在发生安全违规期间关闭公共接口，并通过专用网络解决问题。

## 主要功能

 * 通过我们的专用网络，可以免费与服务器通信并管理服务器。VPN 是此专用网络的网关。
 * 我们提供了 SSL VPN 和 PPTP VPN 选项。
 * 访问点遍布全球，可创建最佳、最快的访问和交互。IBM Cloud 目前在许多城市拥有 VPN 访问点。
 * 请访问 http://www.softlayer.com/vpn-access，以获取 {{site.data.keyword.BluSoftlayer_notm}} 专用网络的 VPN 访问点列表。

## 工作方式

如果使用 VPN 访问，那么可通过两种方法连接到专用网络并管理您的服务器和服务。这些选项包括 SSL 和 PPTP VPN 连接。根据您的个人需求或首选项，使用任一方法连接到专用网络。
 
## SSL VPN 连接

SSL VPN 是一种快速访问连接，用于通过浏览器直接连接到我们的专用网络。SSL VPN 与 Windows XP 或更高版本以及 ActiveX、Fedora、Ubuntu 和 Mac OSX 兼容。可以通过单一 URL（允许选择最近的 VPN 端点）在全球范围内访问我们的专用网络。

## SSL VPN 子网限制

SSL VPN 客户机在使用子网填充其路由表时，存在硬性的“64 个子网”限制。如果帐户的子网数量超过 64 个，请确保修改 SSL VPN 许可权以使用手动子网分配。否则，可能导致无法通过 SSL VPN 访问某些子网。

## PPTP VPN 连接

通过 PPTP VPN，您可以使用特定于操作系统的客户机软件，从台式机或专用设备（例如，防火墙或路由器）安全地连接到专用网络。目前，我们为 Windows XP 或更高版本、Fedora、Ubuntu 和 Mac OSX 提供 VPN 连接。PPTP 连接选项专门为那些需要连接整个办公室或无法使用 SSL VPN 选项进行连接的用户而设计。只与设置 VPN 连接时可能选择的单个数据中心建立 PPTP 连接。

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# VPN 常见问题
{:#vpn-faq}

## 什么是 IBM Cloud VPN？
{:#what-is-ibm-cloud-vpn}
{:faq}

IBM Cloud VPN 访问旨在允许用户通过 IBM Cloud 专用网络安全地远程管理所有服务器。通过建立从您的位置到专用网络的 VPN 连接，便可以使用加密的 VPN 隧道进行带外管理和服务器急救。通过 VPN 访问，您可以：

* 使用 SSL 或 IPSEC 建立与专用网络的 VPN 连接
* 使用 SSH 或 RDP 通过服务器的专用 10.x.x.x IP 地址来访问服务器
* 连接到服务器的 IPMI IP 地址以满足其他服务器管理或急救需求。


## SSL VPN 是否还执行 PPTP、IPSEC 或其他 VPN 协议？
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

SSL VPN 网关目前使用基于浏览器的 SSL VPN 插件或专有客户机来创建连接。我们将继续提供用于连接专用网络的更多 VPN 连接选项。为便于使用并实现兼容，已选择 SSL VPN。PPTP 已弃用。请参阅 [PPTP VPN 弃用](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)以获取更多信息。



## 是否可以通过 SSL VPN 网关从远程位置安装 NAS/FTP 服务器？
{:#can-i-mount-nas-ftp-remotely}
{:faq}

不能...您只能通过 SSL VPN 网关访问自己的专用 VLAN 和服务器。如果要从 NAS/FTP 卷下载数据，必须先将数据移到服务器，然后再通过 VPN 将数据移出到远程位置。

为安全起见，只允许数据中心内的服务器访问用于提供服务（DNS、Update、NAS 或 Lockbox）的服务器。


## 由哪个供应商创建 SSL VPN 以及 SSL VPN 如何工作？
{:#what-vendor-makes-ssl-vpn}
{:faq}

我们的 SSL VPN 网关是来自 Array Networks 的安全产品。该网关本身通过客户门户网站运行 RADIUS 来更新用户和密码。如果您希望添加用户并向用户授予 SSL VPN 访问权，请在客户门户网站中创建一个新用户，并启用 SSL VPN 许可权。


## SSL 与 PPTP VPN 有何差别？
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL VPN** 允许用户创建从远程桌面到 {{site.data.keyword.BluSoftlayer_notm}} 专用网络的安全隧道。它与多种操作系统兼容。

**PPTP VPN** 允许使用相同的安全隧道，但要在用户台式机或专用设备上使用专业客户机软件进行连接。但是，PPTP 已弃用。请参阅 [PPTP VPN 弃用](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)以获取更多信息。

## 为何不能为 PPTP VPN 添加更多用户？
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP 已弃用。请参阅 [PPTP VPN 弃用](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)以获取更多信息。

## 用户在客户门户网站中的 VPN 管理状态有哪些可用类别？
{:#what-are-available-categories-vpn-management}
{:faq}

客户状态类别包括用户能够更新的类别和可自动显示的类别。这些类别包括：

* **活动** - 用户有权根据帐户管理员设置的许可权来访问[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 和 VPN。此状态可随时手动选择或更改。
* **已禁用** - 用户无权访问帐户上的任何许可权或预订，包括[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 和 VPN。如果此状态是帐户上的其他用户设置为禁用的，那么可以随时对其进行手动选择和/或更改。
* **仅限 VPN** - 用户只有权访问 VPN 连接，而无权访问[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/)。此状态可随时手动选择或更改。
* **不活动** - 用户在过去 60 天内未使用[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 或 VPN。这是系统生成的状态。
* **cancel_pending** - 帐户上的管理员已取消此用户，并且当前正在处理该取消操作。这是系统生成的状态。

## 如何设置 SSL VPN？
{:#how-do-i-set-up-ssl-vpn}
{:faq}

有关详细的指示信息，请参阅[连接到 SSL VPN - Windows 7 和更高版本](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7)。



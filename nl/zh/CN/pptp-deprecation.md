---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# PPTP VPN 弃用
{:#pptp-vpn-deprecation}

自 2018 年 6 月 12 日起已弃用 PPTP VPN，并不再向客户提供。感谢您的关注。要了解一些可能的替代方法，请继续阅读。

## 什么是 VPN？
{:#pptp-vpn-deprecation-what-is-vpn}
通过 VPN 访问，用户可以使用 IBM Cloud 专用网络来远程安全地管理所有服务器。通过建立从您的位置到专用网络的 VPN 连接，便可以使用加密的 VPN 隧道进行带外管理和服务器急救。通过 VPN 访问，您可以：

* 通过 SSL、**PPTP** 或 IPSec 建立到专用网络的 VPN 连接
* 使用 SSH 或 RDP 通过服务器的专用 10.x.x.x IP 地址来访问服务器
* 连接到服务器的 IPMI IP 地址以满足其他服务器管理或急救需求

## PPTP 弃用
{:#pptp-deprecation-vpn}
随着其他 VPN 选项越来越安全和多功能化，对 PPTP 的需求已经越来越少了。{{site.data.keyword.BluSoftlayer_notm}} 提供了几种其他选项，比如 SSL 或 IPSec，它们比 PPTP 更先进、更具保护性。

**由于这些原因，{{site.data.keyword.BluSoftlayer_notm}} 自 2018 年 6 月 12 日起不再提供 PPTP。**
{:important}


## 常见问题
{:#pptp-vpn-deprecation-faq}

**问：为什么要弃用 PPTP？**

**答：**为了提供最高品质的保护，{{site.data.keyword.BluSoftlayer_notm}} 决定停止使用 PPTP。{{site.data.keyword.BluSoftlayer_notm}} 希望信守对客户的承诺：他们的隐私和数据的安全性至关重要。 

**问：除了 PPTP 之外，还有哪些可用的其他 VPN 访问类型？**

**答：**{{site.data.keyword.BluSoftlayer_notm}} 提供了几个选项，只需简单配置即可使用。
  1. SSL VPN 是一种快速访问连接，用于通过浏览器直接连接到我们的专用网络。SSL VPN 与 Windows XP 或更高版本以及 ActiveX、Fedora、Ubuntu 和 Mac OSX 兼容。可以通过单一 URL（允许选择最近的 VPN 端点）在全球范围内访问我们的专用网络。有关如何使用此选项的更多详细信息，请参阅[设置 SSL VPN 连接](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections)。
  2. IPSec 是一套协议，用于对两个位置之间的所有 IP 流量进行认证和加密。它只允许在网络上传递受信任数据，除此之外均视为不安全。有关 IPSec 的更多常规信息，请参阅[设置 IPSec VPN](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn)，以及其他一些有关如何使用此服务的[参考文档](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)。 

**问：如果我的业务活动需要使用 PPTP，那么该怎么办？**

**答：**如果需要使用 PPTP 来满足您的业务需求，有几个选项可以使用。**并非所有可能的选项都包含在此。请注意，以下选项需要完整配置两个端点。配置这些选项由客户来负责。**
  1. Virtual Router Appliance。Virtual Router Appliance 也称为 Vyatta，可用作您的环境的网关和路由器。它包含由子网组成的区域。在区域之间设置了防火墙规则，以便各个区域可以相互通信。对于不需要与其他区域进行通信的区域，无需防火墙规则，因为所有数据包都会被丢弃。有关如何使用此服务的更多详细信息，请参阅 [Virtual Router Appliance 入门](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance)。 
  2. FSA 防火墙。FortiGate Security Appliance (FSA) 10Gbps 是一种硬件防火墙，可配置用于保护公用网络和专用网络中多个 VLAN 上的流量。在客户门户网站中，它被称为“多 VLAN 防火墙”。有关如何使用此服务的更多详细信息，请参阅 [FSA 10 Gbps 入门](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps)。 
 
在 {{site.data.keyword.BluSoftlayer_notm}} 停止提供 PPTP 服务之后，如果需要使用该服务来满足您的业务需求，那么可以探索以上这几个可能的选项。承蒙惠顾，不胜感激。
{:note}

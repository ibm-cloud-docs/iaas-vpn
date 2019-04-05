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

# PPTP VPN 淘汰
{:#pptp-vpn-deprecation}

PPTP VPN 自 2018 年 6 月 12 日起淘汰，不再提供給客戶。謝謝您的關注。若要找出部分可能的替代方案，請繼續閱讀。

## 何謂 VPN？
{:#pptp-vpn-deprecation-what-is-vpn}
VPN 存取可讓使用者透過 IBM Cloud 專用網路，從遠端安全地管理所有伺服器。從您的位置至專用網路的 VPN 連線，容許透過已加密的 VPN 通道進行頻外管理，以及伺服器救援。使用 VPN 存取，您可以：

* 透過 SSL、**PPTP** 或 IPSec 建立與專用網路的 VPN 連線
* 透過 SSH 或 RDP，以伺服器的專用 10.x.x.x IP 位址存取伺服器
* 連接至伺服器的 IPMI IP 位址，以處理其他伺服器管理或救援需求

## PPTP 淘汰
{:#pptp-deprecation-vpn}
由於其他 VPN 選項日趨安全且多用途，對於 PPTP 的需要已減少。{{site.data.keyword.BluSoftlayer_notm}} 提供數個比 PPTP 更準確且更具保護力的其他選項，例如 SSL 或 IPSec。

**因此，{{site.data.keyword.BluSoftlayer_notm}} 自 2018 年 6 月 12 日起不再提供 PPTP。**
{:important}


## 常見問題
{:#pptp-vpn-deprecation-faq}

**問：PPTP 為什麼淘汰？**

**答：**為了提供最高品質的保護，{{site.data.keyword.BluSoftlayer_notm}} 已停止使用 PPTP。{{site.data.keyword.BluSoftlayer_notm}} 希望維護對客戶的承諾：客戶的隱私權與資料的安全性是最重要的事。 

**問：除了 PPTP 之外有什麼可用的其他 VPN 存取類型？**

**答：**{{site.data.keyword.BluSoftlayer_notm}} 提供數個選項，這些只需要簡單的配置。
  1. SSL VPN 是一種快速存取的連線，可將您直接從瀏覽器連接至我們的專用網路。SSL VPN 與 Windows XP 或更高版本、ActiveX、Fedora、Ubuntu 及 Mac OSX 相容。您可以透過單一 URL，在全球各地存取我們的專用網路，這可讓您選擇最接近的 VPN 端點。請參閱[設定 SSL VPN 連線](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections)，以取得開始使用這個選項的相關詳細資料。
  2. IPSec 是一套通訊協定，其設計是用來針對兩個位置之間的所有 IP 資料流量進行鑑別與加密。它可讓受信任的資料通過在其他方面被視為不安全的網路。如需有關 IPSec 的一般資訊，請參閱[設定 IPSec VPN](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) 及其他[參考文件](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)，以便開始使用本服務。 

**問：我的商業實務需要 PPTP 怎麼辦？**

**答：**如果因為您的商業需要，必須使用 PPTP，有數種選項可用。**此處無法包羅所有可能的選項。請注意，下列選項需要兩個端點都進行完整配置。客戶需要負責配置這些選項。**
  1. Virtual Router Appliance。Virtual Router Appliance 也稱為 Vyatta，會充當您環境的閘道與路由器。它包含由子網路組成的區域 (zone)。在區域之間設定了防火牆規則，以便與彼此通訊。對於不需要與其他區域通訊的區域，不需要防火牆規則，因為所有封包都將被捨棄。請參閱[開始使用 Virtual Router Appliance](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance)，以取得開始使用本服務的相關詳細資料。 
  2. FSA 防火牆。FortiGate Security Appliance (FSA) 10Gbps 是硬體防火牆，它可以配置來保護多個 VLAN 上的資料流量，公用與專用網路皆可。在「客戶入口網站」中，它稱為「多重 VLAN 防火牆」。請參閱[開始使用 FSA 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps)，以取得開始使用本服務的相關詳細資料。 
 
先前的選項只是在 {{site.data.keyword.BluSoftlayer_notm}} 不在提供服務之後，因為您的商業需要而必須使用 PPTP 時，可以探索的一些可能性。感謝您的業務往來。
{:note}

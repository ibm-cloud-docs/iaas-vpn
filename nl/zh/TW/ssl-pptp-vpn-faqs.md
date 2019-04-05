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

# VPN 常見問題
{:#vpn-faq}

## 何謂 IBM Cloud VPN？
{:#what-is-ibm-cloud-vpn}
{:faq}

IBM Cloud VPN 存取的設計是要容許使用者透過 IBM Cloud 專用網路，安全地遠端管理所有伺服器。從您的位置至專用網路的 VPN 連線，容許透過已加密的 VPN 通道進行頻外管理，以及伺服器救援。使用 VPN 存取，您可以：

* 使用 SSL 或 IPSEC 建立與專用網路的 VPN 連線。
* 使用 SSH 或 RDP，以伺服器的專用 10.x.x.x IP 位址存取伺服器。
* 連接至伺服器的 IPMI IP 位址，以處理其他伺服器管理或救援需求。


## SSL VPN 是否也執行 PPTP、IPSEC 或其他 VPN 通訊協定？
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

目前 SSL VPN 閘道會使用瀏覽器型 SSL VPN 外掛程式或專有用戶端來建立連線。我們將繼續帶給專用網路更多的 VPN 連線功能選項。選取 SSL VPN 是為了易於使用及相容性。PPTP 已淘汰。如需相關資訊，請參閱 [PPTP VPN 淘汰](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)。



## 是否可以透過 SSL VPN 閘道，從我的遠端位置裝載 NAS/FTP 伺服器？
{:#can-i-mount-nas-ftp-remotely}
{:faq}

不，您只能從 SSL VPN 閘道存取您的專用 VLAN 及伺服器。如果想要從 NAS/FTP 磁區下載資料，則您必須將資料移至您的伺服器，然後透過 VPN 移出至遠端位置。

基於安全原因，只容許位於資料中心內的伺服器存取提供服務（DNS、「更新」、NAS、Lockbox）的伺服器。


## 哪個供應商建立 SSL VPN？它如何運作？
{:#what-vendor-makes-ssl-vpn}
{:faq}

我們的 SSL VPN 閘道是來自 Array Networks 的安全產品。閘道本身會執行半徑，以從我們的「客戶入口網站」更新使用者及密碼。如果您想要新增使用者，並將 SSL VPN 存取提供給他們，請在客戶入口網站內建立新使用者，並啟用 SSL VPN 權限。


## SSL 與 PPTP VPN 之間有什麼差異？
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL VPN** 可讓使用者建立從遠端桌面到 {{site.data.keyword.BluSoftlayer_notm}} 專用網路的安全通道。它與各種作業系統相容。

**PPTP VPN** 容許相同的安全通道，但在使用者的桌面或專用裝置上會使用特殊化的用戶端軟體來進行連接。不過，PPTP 已淘汰。如需相關資訊，請參閱 [PPTP VPN 淘汰](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)。

## 為何無法新增 PPTP VPN 的其他使用者？
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP 已淘汰。如需相關資訊，請參閱 [PPTP VPN 淘汰](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)。

## 「客戶入口網站」內的使用者 VPN 管理狀態有哪些可用種類？
{:#what-are-available-categories-vpn-management}
{:faq}

客戶狀態種類包括能夠由使用者更新的種類，以及可能會自動顯示的種類。其中包括：

* **作用中** - 使用者能根據帳戶管理者所設定的許可權，存取[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 和 VPN。您可以隨時手動選取或變更此狀態。
* **已停用** - 使用者無法存取帳戶上的任何許可權或訂閱，包括[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 和 VPN。如果已由帳戶上的另一位使用者設定為停用，則可以隨時手動選取及/或變更此狀態。
* **僅限 VPN** - 使用者只能存取 VPN 連線功能，而無法存取[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/)。您可以隨時手動選取或變更此狀態。
* **非作用中** - 使用者在過去 60 天內未使用[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 或 VPN。這是系統產生的狀態。
* **擱置取消** - 帳戶上的管理者已取消此使用者，而且目前正在處理取消作業。這是系統產生的狀態。

## 如何設定 SSL VPN？
{:#how-do-i-set-up-ssl-vpn}
{:faq}

如需詳細指示，請參閱[連接至 SSL VPN - Windows 7 及更高版本](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7)。



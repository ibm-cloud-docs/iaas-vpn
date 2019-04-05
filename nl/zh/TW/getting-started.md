---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, IBM Cloud VPN, user account

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 開始使用 Virtual Private Networking (VPN)
{:#gettingstarted-with-virtual-private-networking}

## 何謂 IBM Cloud VPN？
{:#what-is-ibmcloud-vpn}


VPN 存取可讓使用者透過 IBM Cloud 專用網路，從遠端安全地管理所有伺服器。從您的位置至專用網路的 VPN 連線，容許透過已加密的 VPN 通道進行頻外管理，以及伺服器救援。使用 VPN 存取，您可以：

* 透過 SSL 或 IPSec 建立與專用網路的 VPN 連線。
* 透過 SSH 或 RDP，以伺服器的專用 10.x.x.x IP 位址存取伺服器。
* 連接至伺服器的 IPMI IP 位址，以處理其他伺服器管理或救援需求。

**PPTP VPN 服務自 2018 年 6 月 12 日起淘汰，如[我們的宣布](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)中所述。**
{:deprecated}

許多服務都需要透過專用網路進行存取，而 VPN 是容許專用網路存取的一種方法。VPN 適用於您需要登入專用網路、執行工作，然後登出的情況。例如，聯繫伺服器的 KVM 便經常需要此存取作業。

每一個使用者帳戶都可以獲得 VPN 存取，而且可以針對需要存取的子網路加以限制。您必須已啟用 VPN 存取，且必須建立 VPN 密碼，才能登入 VPN。

## 啟用每個使用者的 VPN 存取
{:#enable-user-vpn-access}

若要開始使用，您需要在需要 VPN 存取的每一個帳戶上，啟用 VPN 存取。每個帳戶一開始時會**停用** VPN 存取，包括您的團隊的主要帳戶也是如此。若要啟用 VPN 存取，請遵循下列步驟：

1. 移至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 的**帳戶 -> VPN 存取**。
* 您會在那裡找到每個可能 VPN 使用者的列，並且在 **VPN 存取**直欄中會有一個鏈結。
* 如果使用者尚未啟用 VPN 存取，則鏈結會顯示「無」。
* 如果使用者的 VPN 存取鏈結顯示 **SSL**，則表示使用者已啟用 VPN 存取。

![Softlayer 入口網站 VPN 存取表格](images/vpnaccess01.png)

1. 若要啟用或變更針對特定使用者允許的 VPN 存取類型，請按一下 **VPN 存取**直欄下的鏈結。
* 在下一頁，您可以啟用適合每個使用者的 VPN 存取類型。  

![指派 VPN 類型存取給使用者](images/vpntype01.png)

## 設定 VPN 密碼
{:#set-vpn-password}

下一步是建立 VPN 密碼。每一位使用者都可以在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 中建立及更新其 VPN 密碼。如果要這麼做，請在右上方選取您的名稱，這會將您帶到**編輯設定檔**頁面。您也可以選取**帳戶 -> 使用者**，然後選取您的使用者名稱。

      附註：鏈結會顯示「主要使用者」。這個鏈結將為子使用者顯示您的名稱。

在**編輯使用者設定檔**頁面上，只需向下捲動並起始設定或更新 VPN 密碼即可。

![ 編輯設定檔 VPN 密碼欄位](images/vpnpasswordfields.png)

## 登入 VPN
{:#login-to-the-vpn}

既然已建立 VPN 存取，您可以登入了。

1. 若要登入 SSL VPN，請造訪 [vpn.softlayer.com](https://vpn.softlayer.com/) 然後選取任何登入點。您可以使用任何 VPN 存取點，而且會獲得對於所有資料中心裡專用網路的相同存取權。
* 如果您在登入一個位置時遇到問題，請嘗試另一個位置。
* 或者，也可以使用獨立式用戶端 SSL VPN 來登入。

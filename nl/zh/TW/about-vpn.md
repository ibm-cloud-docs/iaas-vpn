---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 關於 VPN
{:#about-iaas-vpn}

VPN 存取可讓您透過 IBM Cloud 專用網路，遠端管理與您帳戶相關聯的所有伺服器及服務。從您的位置至專用網路的 VPN 連線，容許透過已加密的 VPN 通道進行**頻外管理以及伺服器救援**。

使用專用網路進行通訊就本質上更安全。它可讓您彈性限制公用存取，但仍可以管理伺服器。您帳戶上的任何使用者都可獲授與 VPN 存取（以 SSL 方式提供）。透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 進行的 VPN 互動，容許在使用者層次進行 VPN 存取自訂。

## 有哪些方法可以使用 SSL VPN？
{:#ways-to-use-iaas-vpn}

這種頻外 Secure Gateway 可讓您透過專用網路存取伺服器。常見用法如下：

* 針對 SSH 或 RDC 連接至伺服器的專用 IP 位址 (10.x.x.x)。
* 連接至 IPMI 卡以進行遠端主控台/存取/監視。
* 在 Windows 或 Red Hat 中，從家用或工作 PC 裝載磁碟機以方便使用。
* 關閉資料庫伺服器上的公用介面，並透過專用網路進行管理。
* 第一次設定伺服器時關閉公用介面。
* 在重要安全更新期間關閉公用介面。
* 在安全侵害期間關閉公用介面，並透過專用網路來解決問題。

## 重要特性
{:#iaas-vpn-key-features}

 * 我們的專用網路提供一種無成本的方式來與伺服器進行通訊以及管理伺服器。VPN 是此專用網路的閘道。
 * 全球的存取點能建立最佳且最快速的存取與互動。IBM Cloud 目前在許多城市都有 VPN 存取點。
 * 如需取得 {{site.data.keyword.BluSoftlayer_notm}} 專用網路的 VPN 存取點清單，請造訪 `http://www.softlayer.com/vpn-access`。

## 如何運作
{:#iaas-vpn-how-it-works}

使用 VPN 存取時，請使用 SSL 來與專用網路連接，並管理您的伺服器及服務。 

## SSL VPN 連線
{:#iaas-vpn-ssl-vpn-connections}

SSL VPN 是一種快速存取的連線，可將您直接從瀏覽器連接至我們的專用網路。SSL VPN 與 Windows XP 或更高版本、ActiveX、Fedora、Ubuntu 及 Mac OSX 相容。您可以透過單一 URL，在全球各地存取我們的專用網路，這可讓您選擇最接近的 VPN 端點。

## SSL VPN 子網路限制
{:#iaas-vpn-ssl-vpn-subnet-limit}

SSL VPN 用戶端在可以用來移入其遞送表這方面，有一項強制性的 64 個子網路限制。如果您的帳戶有超過 64 個子網路，請務必修改 SSL VPN 許可權，以使用手動子網路指派。否則，部分子網路可能無法透過 SSL VPN 聯繫。

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 關於 VPN

VPN 存取可讓您透過 IBM Cloud 專用網路，遠端管理與您帳戶相關聯的所有伺服器及服務。從您的位置至專用網路的 VPN 連線，容許透過已加密的 VPN 通道進行頻外管理，以及伺服器救援。

使用專用網路進行通訊就本質上更安全。它可讓您彈性限制公用存取，但仍可以管理伺服器。您帳戶上的任何使用者都可獲授與 VPN 存取（同時以 SSL 及 PPTP 方式提供）。透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 進行的 VPN 互動，容許在使用者層次進行 VPN 存取自訂。

## 有哪些方法可以使用 SSL VPN？

這種頻外 Secure Gateway 可讓您透過專用網路存取伺服器。常見用法如下：

* 針對 SSH 或 RDC 連接至伺服器的專用 IP 位址 (10.x.x.x)。
* 連接至 IPMI 卡以進行遠端主控台/存取/監視。
* 在 Windows 或 Red Hat 中，從家用或工作 PC 裝載磁碟機以方便使用。
* 關閉資料庫伺服器上的公用介面，並透過專用網路進行管理。
* 第一次設定伺服器時關閉公用介面。
* 在重要安全更新期間關閉公用介面。
* 在安全侵害期間關閉公用介面，並透過專用網路來解決問題。

## 重要特性

 * 我們的專用網路提供一種無成本的方式來與伺服器進行通訊以及管理伺服器。VPN 是此專用網路的閘道。
 * 我們提供 SSL VPN 及 PPTP VPN 選項。
 * 全球的存取點能建立最佳且最快速的存取與互動。IBM Cloud 目前在許多城市都有 VPN 存取點。
 * 如需取得 {{site.data.keyword.BluSoftlayer_notm}} 專用網路的 VPN 存取點清單，請造訪 http://www.softlayer.com/vpn-access。

## 如何運作

使用 VPN 存取時，有兩種方式可用來與專用網路連接，並管理您的伺服器及服務。這些選項包括 SSL 及 PPTP VPN 連線。請根據您的個別需要或喜好，使用任一種方法連接至專用網路。
 
## SSL VPN 連線

SSL VPN 是一種快速存取的連線，可將您直接從瀏覽器連接至我們的專用網路。SSL VPN 與 Windows XP 或更高版本、ActiveX、Fedora、Ubuntu 及 Mac OSX 相容。您可以透過單一 URL，在全球各地存取我們的專用網路，這可讓您選擇最接近的 VPN 端點。

## SSL VPN 子網路限制

SSL VPN 用戶端在可以用來移入其遞送表這方面，有一項強制性的 64 個子網路限制。如果您的帳戶有超過 64 個子網路，請務必修改 SSL VPN 許可權，以使用手動子網路指派。否則，部分子網路可能無法透過 SSL VPN 聯繫。

## PPTP VPN 連線

PPTP VPN 可讓您從桌面使用 OS 特有用戶端軟體，或使用專用裝置（例如防火牆或路由器），安全地連接至專用網路。我們目前針對 Windows XP 或更新版本、Fedora、Ubuntu 及 Mac OSX 提供 VPN 連線功能。PPTP 連線選項設計的對象，是尋求連接整個辦公室的人，或是無法使用 SSL VPN 選項進行連接的人。會與單一資料中心建立 PPTP 連線，您可以在設定 VPN 連線時選擇資料中心。

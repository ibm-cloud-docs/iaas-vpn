---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 設定 Windows 7 的 PPTP VPN

PPTP VPN 連線容許從桌面或專用裝置，遠端連線到 {{site.data.keyword.BluSoftlayer_notm}} 專用網路。透過 PPTP 連接至「專用網路」適用於多個作業系統，包括 Windows 7。使用者可以在設定期間輸入資料中心的唯一目的地位址，來連接任何 {{site.data.keyword.BluSoftlayer_notm}} 資料中心。請遵循下面的步驟，以在 Windows 7 中設定 PPTP VPN 連線。

## 設定 PPTP VPN 連線

1. 參閱 Microsoft 的[使用方法頁面](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window}，以到達設定遠端連線的畫面。

2. 在網際網路位址欄位中，輸入所需資料中心的目的地位址。請參閱下表，以取得現行 IBM Cloud 資料中心的適當位址。

|資料中心位置|資料中心網際網路位址|
|---|---|
|達拉斯，德克薩斯州|pptpvpn.dal01.softlayer.com|
|西雅圖，華盛頓州|pptpvpn.sea01.softlayer.com|
|聖荷西，加州|pptpvpn.sjc01.softlayer.com|
|華盛頓特區|pptpvpn.wdc01.softlayer.com|
|阿姆斯特丹，北荷蘭省|pptpvpn.ams01.softlayer.com|
|新加坡，新加坡|pptpvpn.sng01.softlayer.com|
|休士頓，德克薩斯州|pptpvpn.hou02.softlayer.com|
|香港，香港|pptpvpn.hkg02.softlayer.com|
|墨爾本，澳洲|pptpvpn.mel01.softlayer.com|
|倫敦，英國|pptpvpn.lon02.softlayer.com|
|巴黎，法國|pptpvpn.par01.softlayer.com|
|多倫多，加拿大|pptpvpn.tor01.softlayer.com|
|東京，日本|pptpvpn.tok02.softlayer.com|

3\. 在**目的地名稱**欄位中，輸入連線的識別性名稱。

**附註**：建議使用資料中心位置作為目的地名稱。

4\. 在**使用者名稱**欄位中，輸入您的[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 使用者名稱。

5\. 在**密碼**欄位中，輸入您的 **VPN 密碼**。

6\. 按一下**連接**按鈕。

7\. 現在，在您的電腦上，您需要停用遠端閘道，以連接至網際網路及 VPN。

8\. 按一下**開始**，然後開啟**控制台** -> **網路和共用中心** -> **變更介面卡設定**。

9\. 用滑鼠右鍵按一下 PPTP VPN 連線，然後按一下**內容**。

10\. 取消勾選 TCP/IPv6 方框，然後依序按一下 TCP/IPv4 及「內容」。

11\. 按一下**進階**按鈕。

12\. 取消勾選**使用遠端網路的預設閘道**方框，然後選取**確定**。

---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 設定 Mac OS X 10.X 的 PPTP VPN

PPTP VPN 連線容許從桌面或專用裝置，遠端連線到 {{site.data.keyword.BluSoftlayer_notm}} 專用網路。透過 PPTP 連接至「專用網路」適用於多個作業系統，包括 Mac OS X。使用者可以在設定時輸入資料中心的唯一目的地位址，來連接任何 {{site.data.keyword.BluSoftlayer_notm}} 資料中心。請遵循下面的步驟，以在 Mac OS X 中設定 PPTP VPN 連線。

## 設定 PPTP VPN 連線

* 從 **Apple 功能表**下拉清單中選取**系統喜好設定**。
* 在「網際網路與網路」區段，按一下**網路**圖示。
* 按一下**連線**功能表底端的**加號**圖示。此時會出現一個蹦現方框，讓您建立 VPN 連線。
* 建立「VPN 連線」。
  * 從**介面**下拉清單選取 **VPN**。
  * 從 **VPN 類型**下拉清單選取 **PPTP**。
  * 在**服務名稱**欄位中，輸入連線的**敘述性標題**。
  * **附註**：建議使用「資料中心」位置作為「服務名稱」的一部分。
  * 按一下**建立**按鈕。
* 在「連線」功能表中按一下剛剛建立的連線。
* 在**伺服器位址**欄位中，輸入所需資料中心的**目的地位址**。請參閱下表，以取得現行 {{site.data.keyword.BluSoftlayer_notm}} 資料中心的適當位址。
* 在**帳戶名稱**欄位中，輸入**客戶入口網站使用者名稱**。
* 完成「鑑別設定」。
  * 按一下**鑑別設定**按鈕。會出現提示鑑別 VPN 的蹦現方框。
  * 在**密碼**欄位中，輸入您的**客戶 VPN 密碼**。
  * 按一下**確定**按鈕。
* 更新「VPN 資料流量」設定。
  * 按一下**進階**按鈕。
  * 確定未選取「階段作業」區段中的**透過 VPN 連線傳送所有資料流量**勾選框。
  * 按一下**確定**按鈕。
* 選取**在功能表列中顯示 VPN 狀態**勾選框。
* 按一下「套用」按鈕。只要使用 VPN 功能表列項目，即可隨時建立 VPN 連線。

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

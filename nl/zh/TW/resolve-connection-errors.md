---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN, Internet Explorer caching, Internet Explorer, Windows

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 解決使用 Windows 連接至 SSL VPN 的錯誤
{:#resolve-errors-connecting-to-ssl-vpn-with-windows}

如果您在使用 Windows 連接至 SSL VPN 時收到錯誤，則可以使用下列步驟進行疑難排解：

1. 在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 中檢查是否有適當的認證和 SSL 許可權。
2. 在 PC 上檢查您的時間/時間/日期/時區/DST。
3. 您必須接受並安裝 ActiveX Applet。
4. 關閉蹦現畫面封鎖程式，它們可能會封鎖 ActiveX Applet。
5. 檢查個人防火牆 - 容許 ActiveX。
6. 容許 Internet Explorer 快取 - 在 IE 中（選取**工具 -> 網際網路**，然後選取**選項 -> 設定**）。
7. 只使用 Internet Explorer (IE) 瀏覽器（檢查更新）。
8. 嘗試系統重新開機。

連接妥當之後，系統匣會出現 "A"。

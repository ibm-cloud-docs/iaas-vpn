---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 設定 SSL VPN 連線

Windows、Linux Fedora 及 Linux 需要個別的連線指示，如本文件所示。以下是一些如何使用 SSL VPN 連線的範例：

* 使用「遠端桌面」連接至伺服器的後端 IP 位址 (10.4.X.X)，以管理您的 Windows 2003 伺服器。
* 使用 SSH 連接至伺服器的後端 IP 位址 (10.4.X.X)，以管理您的 UNIX 伺服器。
* 使用 IPMI 用戶端，控制使用後端 IPMI 位址 (10.4.X.X) 的伺服器。連接之後，您可以前往 http://downloads.service.softlayer.com 下載 IPMI 用戶端工具。
  * **附註：**IPMIVView 需要安裝 Java。http://www.sun.com/java/
* 先在後端 IP 上測試網站，然後才能提供到公用 IP 上。
* 伺服器與您的住家/辦公室之間安全資料的檔案傳送。
* 將伺服器上的配置檔備份到您的住家/辦公室。
* 安全地連接至我們的 Web 入口網站，網址為 `http://manage.service.softlayer.com`。

## Windows (Internet Explorer)

1. 開啟 Internet Explorer，並導覽至 `http://www.softlayer.com/vpn-access`。
* 輸入您的使用者名稱和密碼之後，系統會提示您安裝 ActiveX 外掛程式。您必須安裝此外掛程式才能連接至後端網路。 
* 您也必須在工作站上具有管理權限，才能安裝 ActiveX 外掛程式。如果您沒有安裝此外掛程式的權限，請要求本端「系統管理者」為您安裝。 
* 安裝 ActiveX 外掛程式之後，Array SSL VPN 網路連接器會啟動並建立與 VPN 裝置的連線。如果成功，您的作業列會出現紅色的 '**A**'。您可以隨時按一下 '**A**'，以查看 SSL VPN 連線的狀態：其狀態、已指派的 IP 位址、已指派的 DNS 伺服器、網路路徑及連接的時間。 
* 您隨時可以將瀏覽器階段作業最小化，並在專用網路上安全地繼續使用其他應用程式。 
* 完成之後，請先選取右側的中斷連線按鈕來中斷連線，或是直接關閉視窗。

## Linux Fedora (FireFox)

建議您以 root 使用者身分執行所有指令。(`setuid root`)

1. 從 `http://java.com/en/download/manual.jsp` 下載 Java。這是 Linux 版的自動解壓縮檔。
* 關閉 FireFox。
* 將檔案移至您要安裝 Java 的位置（通常位於 `/usr/local`）。
* 使用指令 `chmod +x jre-6u1-linux-i586.bin` 讓檔案成為可執行檔。
* 使用指令 `./jre-6u1-linux-i586.bin` 執行安裝程式。
* 同意條款，然後進行安裝。
* 安裝完成之後，您現在必須建立符號鏈結。

## Linux 範例
```
cd /usr/lib/firefox-1.0.4/plugins/
ln -s /usr/local/jre-6u1/plugin/i386/ns7/libjavaplugin_oji.so .
```

1. 開啟 Firefox，並移至 `http://www.softlayer.com/vpn-access`。
* 使用客戶入口網站使用者名稱及密碼登入。
* 連接之後，請選取**網路**標籤。
* 您應該會看到連接/安裝按鈕。請選取它，然後系統應該會提示您安裝 Java 元件。
* 讓元件安裝到預設路徑（您可能需要手動建立）。(`/usr/local/array_vpn`)
* 安裝之後，應該會出現一個視窗，指出您已連接。
* 此視窗必須保持開啟狀態才能使用 VPN 通道，但您可以將它最小化。
* 若要測試連線，請對 10.0.80.11 或伺服器的專用位址進行連線測試。如果得到回覆，則表示您已順利連接。
* 完成時，請選取「網路」標籤下的中斷連線按鈕，或直接關閉所有瀏覽器視窗。

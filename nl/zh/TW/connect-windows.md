---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 連接至 SSL VPN - Windows 7 及更高版本

若要連接至 {{site.data.keyword.BluSoftlayer_notm}} SSL VPN，您需要在電腦上執行一些步驟，以確保您可以連接。

**1. 關閉控制台中的「使用者存取控制 (UAC)」**

1. 導覽至**開始 -> 控制台 -> 使用者帳戶 -> 變更使用者帳戶控制設定**。
* 取消勾選**使用 \[使用者帳戶控制 (UAC)\] 來協助保護您的電腦**旁的方框。

**2. 啟用 Administrator 帳戶**

1. 移至**開始 -> 控制台 -> 系統管理工具 -> 電腦管理 -> 本機使用者和群組 -> 使用者**。 
* 在 **Administrator** 使用者按一下滑鼠右鍵，然後選取**內容**。 
* 取消勾選**帳戶已停用**的方框。

**3. 在連接至 SSL VPN 頁面之前，以 Administrator 身分執行 Internet Explorer**

1. 用滑鼠右鍵按一下 Internet Explorer 圖示，然後從功能表中選取**以系統管理員身分執行**。

完成前一個步驟之後，您應該可以登入。 

## 登入

1. 移至 [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access)，然後使用您的入口網站使用者名稱和密碼登入。 
* 確定您的使用者[具有 SSL VPN 存取](edit-users-vpn-access.html)。  
* 此外，也請確定您已設定 VPN 密碼。如果要這麼做，請更新您的[使用者設定檔頁面](https://control.softlayer.com/account/user/profile)，並填寫 **VPN 密碼**方框。

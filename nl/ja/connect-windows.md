---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL VPN への接続 - Windows 7 以上
{:#connect-ssl-vpn-windows7}

{{site.data.keyword.BluSoftlayer_notm}} SSL VPN に接続するには、ご使用のコンピューター上でいくつかのステップを実行して、接続できることを確認する必要があります。

**1. コントロール パネルでユーザーアクセス制御 (UAC) をオフにする**

1. **「スタート」->「コントロール パネル」->「ユーザー アカウント」->「ユーザー アカウント制御設定の変更」**にナビゲートします。
* **「ユーザー アカウント制御を使用すると、問題を起こす可能性があるプログラムからのコンピューターの変更の防止に役立ちます。(Use User Account Control (UAC) to help protect your computer)」**の横にあるボックスの**チェック・マークを外します**。

**2. 管理者アカウントを有効にする**

1. **「スタート」->「コントロール パネル」->「管理ツール」->「コンピューターの管理」->「ローカル ユーザーとグループ」->「ユーザー」**に移動します。 
* **「Administrator」**ユーザーを右クリックして**「プロパティ」**を選択します。 
* **「このアカウントは無効になっています (Account is disabled)」**のボックスのチェック・マークを外します。

**3. SSL VPN ページに接続する前に Internet Explorer を管理者で実行する**

1. Internet Explorer アイコンを右クリックしてメニューから**「管理者として実行」**を選択します。

前のステップが完了していればログインできます。 

## ログイン
{:#connect-windows-login}

1. [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) にアクセスし、自分のポータル・ユーザー名およびパスワードを使用してログインします。 
* 自分のユーザーに [SSL VPN アクセス権限がある](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user)ことを確認します。  
* また、VPN パスワードが設定してあることも確認します。 これを行うには、[ユーザー・プロファイル・ページ](https://control.softlayer.com/account/user/profile)を更新して、**「VPN パスワード (VPN Password)」**というボックスにパスワードを入力します。

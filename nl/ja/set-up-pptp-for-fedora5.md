---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Fedora Core 5 での PPTP のセットアップ

インストールと構成が必要になります。

**1. インストール**
以下のいずれかのコマンドを使用して PPTP と `pptpconfig` GUI をインストールします。
```
# rpm -Uvh http://pptpclient.sourceforge.net/yum/stable/fc5/pptp-release-current.no...
# yum --enablerepo=pptp-stable install pptpconfig
```

**2. 構成**

1. IBM Cloud PPTP 情報:
<table><tr><td>サーバー:</td><td>pptpvpn.dal01.softlayer.com (ダラス)<br/>pptpvpn.sea01.softlayer.com (シアトル)<br/>pptpvpn.wdc01.softlayer.com (ワシントン D.C.)</td></tr><tr><td>ドメイン・ネーム:</td><td>強制ブランク</td></tr><tr><td>ユーザー名:</td><td>(例: SL12345)</td></tr><tr><td>パスワード:</td><td>&nbsp;</td></tr></table>

2. *pptpconfig* を <span style="text-decoration: underline">root として</span>実行します。ウィンドウが表示されます。<br/>
![図 1](images/ss1.jpeg)

3. 「サーバー」タブに、名前、サーバー、ユーザー名、およびパスワードを入力します。

4. 「暗号化」セクションでは、大半のお客様用に機能するよう、すべてをデフォルトのままにします。<br/>
![図 2](images/ss2.jpeg)

5. *「追加」*をクリックします。トンネルがリストに表示されます。

6. トンネルをクリックして選択し、*「開始」*をクリックします。トンネル接続のログと状況を示すウィンドウが表示されます。

7. 接続に失敗すると、詳細情報の収集が必要になる場合があります。そのため、*「その他 (Miscellaneous)」*タブで*「接続デバッグ機能の有効化 (Enable connection debugging facilities)」*をクリックし、*「更新」*をクリックして、再度*「開始」*を試し、エラーが表示されたものすべてについて[「診断 HOWTO (Diagnosis HOWTO)」](http://pptpclient.sourceforge.net/howto-diagnosis.phtml){:new_window}を確認します。<br/>
![図 3](images/ss3.jpeg)

8. 接続が成功すると、「ping テスト」ボタンを試すことができます。ping が失敗した場合は、先に進む前に原因を判別しておく必要があります。ping が機能した場合は、トンネルがアクティブになり、経路指定が可能になります。

9. IBM Cloud のバックエンド・ネットワークで活動中の IP のみを、この VPN トンネルを経由して経路指定する必要があります。トンネルを*停止*し、再度選択し、*「経路指定 (Routing)」*タブの*「クライアントから LAN (Client to LAN)」または「LAN から LAN (LAN to LAN)」*のいずれかをクリックし、*「ネットワーク経路の編集 (Edit Network Routes)」*ボタンを使用して「ネットワーク」に '10.0.0.0/8' を、「名前」に 'SoftLayer' を入力して、再度*「開始」*を試します。ご使用のサーバーのプライベート IP アドレスまたは SoftLayer のプライベート・ネーム・サーバー (10.0.80.11) にアクセスしてみてください。<br/>
![図 4](images/ss4.jpeg)

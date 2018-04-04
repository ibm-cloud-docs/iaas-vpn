---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Windows 7 での PPTP VPN のセットアップ

PPTP VPN 接続により、デスクトップまたは専用デバイスから{{site.data.keyword.BluSoftlayer_notm}}プライベート・ネットワークへのリモート接続が可能になります。PPTP によるプライベート・ネットワークへの接続は、Windows 7 を含め、複数のオペレーティング・システムで使用できます。ユーザーは、セットアップ時にデータ・センターの固有宛先アドレスを入力することにより、どの {{site.data.keyword.BluSoftlayer_notm}} データ・センターにも接続できます。Windows 7 で PPTP VPN 接続をセットアップするには、以下の手順に従ってください。

## PPTP VPN 接続のセットアップ

1. リモート接続をセットアップするための画面にアクセスするには、Microsoft の [How-To ページ](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window}を参照してください。

2. インターネット・アドレス・フィールドに目的のデータ・センターの宛先アドレスを入力します。現行 IBM Cloud データ・センターの適切なアドレスについては、下表を参照してください。

|データ・センターの場所|データ・センターのインターネット・アドレス|
|---|---|
|ダラス、TX|pptpvpn.dal01.softlayer.com|
|シアトル、WA|pptpvpn.sea01.softlayer.com|
|サンノゼ、CA|pptpvpn.sjc01.softlayer.com|
|ワシントン、DC|pptpvpn.wdc01.softlayer.com|
|アムステルダム、NL|pptpvpn.ams01.softlayer.com|
|シンガポール、SG|pptpvpn.sng01.softlayer.com|
|ヒューストン、TX|pptpvpn.hou02.softlayer.com|
|香港、HK|pptpvpn.hkg02.softlayer.com|
|メルボルン、AU|pptpvpn.mel01.softlayer.com|
|ロンドン、GB|pptpvpn.lon02.softlayer.com|
|パリ、FR|pptpvpn.par01.softlayer.com|
|トロント、CA|pptpvpn.tor01.softlayer.com|
|東京、JP|pptpvpn.tok02.softlayer.com|

3\. **「宛先名」**フィールドに接続の識別名を入力します。

**注:** データ・センターの場所を宛先名として使用することをお勧めします。

4\. **「ユーザー名」**フィールドに[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) のユーザー名を入力します。

5\. **「パスワード」**フィールドに**「VPN パスワード」**を入力します。

6\. **「接続」**ボタンをクリックします。

7\. 次に、インターネットと VPN に接続できるように、ご使用のコンピューターでリモート・ゲートウェイを無効にする必要があります。

8\. **「スタート」**をクリックし、**「コントロール パネル」** -> **「ネットワークと共有」** -> **「アダプターの設定の変更」**の順に開きます。

9\. PPTP VPN 接続を右クリックし、**「プロパティ」**をクリックします。

10\. 「TCP/IPv6」ボックスのチェック・マークを外して、「TCP/IPv4」をクリックし、「プロパティ」をクリックします。

11\. **「詳細設定」**ボタンをクリックします。

12\. **「リモート ネットワークでデフォルト ゲートウェイを使う」**ボックスのチェック・マークを外して、**「OK」**をクリックします。

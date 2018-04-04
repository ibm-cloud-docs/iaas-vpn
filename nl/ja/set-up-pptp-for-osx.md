---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mac OS X 10.X での PPTP VPN のセットアップ

PPTP VPN 接続により、デスクトップまたは専用デバイスから{{site.data.keyword.BluSoftlayer_notm}}プライベート・ネットワークへのリモート接続が可能になります。PPTP によるプライベート・ネットワークへの接続は、Mac OS X を含め、複数のオペレーティング・システムで使用できます。ユーザーは、セットアップ時にデータ・センターの固有宛先アドレスを入力することにより、どの {{site.data.keyword.BluSoftlayer_notm}} データ・センターにも接続できます。Mac OS X で PPTP VPN 接続をセットアップするには、以下の手順に従ってください。

## PPTP VPN 接続のセットアップ

* **Apple メニュー**・ドロップダウンから**「システム環境設定」**を選択します。
* 「インターネットとネットワーク (Internet&Network)」セクションで**「ネットワーク」**アイコンをクリックします。
* **「接続」**メニューの下部にある**プラス**・アイコンをクリックします。VPN 接続を作成するためのポップアップ・ボックスが表示されます。
* VPN 接続を作成します。
  * **「インターフェイス」**ドロップダウン・リストから**「VPN」**を選択します。
  * **「VPN タイプ」**ドロップダウン・リストから**「PPTP」**を選択します。
  * **「サービス名」**フィールドに接続の**説明的タイトル**を入力します。
  * **注:** データ・センターの場所をサービス名の一部として使用することをお勧めします。
  * **「作成」**ボタンをクリックします。
* 「接続」メニューで作成した接続をクリックします。
* **「サーバアドレス」**フィールドに、目的のデータ・センターの**宛先アドレス**を入力します。現行 {{site.data.keyword.BluSoftlayer_notm}} データ・センターの適切なアドレスについては、下表を参照してください。
* **「アカウント名」**フィールドに**カスタマー・ポータル・ユーザー名**を入力します。
* 認証設定を完了します。
  * **「認証設定」**ボタンをクリックします。VPN の認証を求めるポップアップ・ボックスが表示されます。
  * **「パスワード」**フィールドに**「カスタマー VPN パスワード」**を入力します。
  * **「OK」**ボタンをクリックします。
* VPN トラフィック設定を更新します。
  * **「詳細設定」**ボタンをクリックします。
  * 「セッション」セクションの**「すべてのトラフィックを VPN 接続経由で送信」**チェック・ボックスが選択されていないことを確認します。
  * **「OK」**ボタンをクリックします。
* **「メニューバーに VPN の状況を表示」**チェック・ボックスを選択します。
* 「適用」ボタンをクリックします。これで、いつでも VPN メニュー・バーを使用して VPN 接続を確立できます。

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

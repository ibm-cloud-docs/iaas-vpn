---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ubuntu での PPTP VPN のセットアップ

PPTP VPN 接続により、デスクトップまたは専用デバイスから{{site.data.keyword.BluSoftlayer_notm}}プライベート・ネットワークへのリモート接続が可能になります。PPTP によるプライベート・ネットワークへの接続は、Ubuntu を含め、複数のオペレーティング・システムで使用できます。ユーザーは、セットアップ時にデータ・センターの固有宛先アドレスを入力することにより、どの{{site.data.keyword.BluSoftlayer_notm}}データ・センターにも接続できます。Ubuntu で PPTP VPN 接続をセットアップするには、以下の手順に従ってください。

## PPTP VPN 接続のセットアップ

Ubuntu で PPTP VPN 接続をセットアップするには、Ubuntu の [VPNClient](https://help.ubuntu.com/community/VPNClient){:new_window} の資料を参照し、以下の情報を使用して接続を完了します。

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

* VPN ゲートウェイまたは URL については、下表を参照して、目的の接続ロケーションに対応するアドレスを確認してください。

* VPN 認証のユーザー名として、**カスタマー・ポータル・ユーザー名**を使用します。
* VPN 認証のパスワードとして、**設定した VPN パスワード**を使用します。

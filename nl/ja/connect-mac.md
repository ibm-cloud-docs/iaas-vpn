---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL VPN への接続 - MAC OSX 10x 以上
{:#connect-ssl-vpn-mac-osx}

Apple Store から最新バージョンの Mac MotionPro クライアント v1.1.7 をインストールします。更新する前に、必ず以前のバージョンをアンインストールしてください。

新しいクライアントをインストールしたら、以下のディレクトリーに移動し、端末アプリケーションを使用して VPN を起動します。 

`/usr/local/motionpro/`

この場所で、以下のコマンドを実行して SSL VPN に接続します。

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

VPN エンドポイントのリストは、[こちら](https://www.softlayer.com/vpn-access)をご覧ください。

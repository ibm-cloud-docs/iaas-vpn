---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN, Internet Explorer caching, Internet Explorer, Windows

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Windows での SSL VPN への接続エラーの解決
{:#resolve-errors-connecting-to-ssl-vpn-with-windows}

Windows での SSL VPN への接続時にエラーが発生する場合は、以下の手順でトラブルシューティングを行うことができます。

1. [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で適切な資格情報と SSL 許可があるかを確認します。
2. ご使用の PC で time/date/time zone/dst を確認します。
3. ActiveX アプレットを受け入れ、インストールする必要があります。
4. ポップアップ・ブロッカーをオフにします - これらは ActiveX アプレットをブロックする可能性があります。
5. パーソナル・ファイアウォールが ActiveX を許可していることを確認します。
6. IE で Internet Explorer キャッシングを許可します (**「ツール」->「インターネット」**を選択し、次に**「オプション」->「設定」**を選択します)。
7. Internet Explorer (IE) ブラウザーのみを使用します (更新を確認)。
8. システム・リブートを試行します。

正しく接続されると、systray に「A」が表示されます。

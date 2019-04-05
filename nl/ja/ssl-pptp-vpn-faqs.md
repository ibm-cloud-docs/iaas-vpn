---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# VPN FAQ
{:#vpn-faq}

## IBM Cloud VPN とは?
{:#what-is-ibm-cloud-vpn}
{:faq}

IBM Cloud VPN アクセスは、ユーザーが IBM Cloud プライベート・ネットワーク経由ですべてのサーバーをリモート側からセキュアに管理できるように設計されています。  お客様のロケーションからプライベート・ネットワークへの VPN 接続により、暗号化された VPN トンネル経由でのアウト・オブ・バンド管理とサーバー・レスキューが可能になります。 VPN アクセスを使用すれば、以下を行うことができます。

* SSL または IPSEC を使用してプライベート・ネットワークへの VPN 接続を確立する
* SSH または RDP を使用してプライベート IP アドレス 10.x.x.x でサーバーにアクセスする
* さらなるサーバー管理やレスキューのニーズに対応するために、サーバーの IPMI IP アドレスに接続する


## SSL VPN は、PPTP、IPSEC、その他の VPN プロトコルも実行しますか?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

現在、SSL VPN ゲートウェイは、接続を作成するために、ブラウザー・ベースの SSL VPN プラグインまたは専有クライアントを使用しています。 今後、さらに多くの VPN 接続オプションをプライベート・ネットワークに提供する予定です。 SSL VPN が選択された理由は、使いやすさと互換性です。PPTP は非推奨になりました。詳しくは、[PPTP VPN の非推奨](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)を参照してください。



## リモート・ロケーションから SSL VPN ゲートウェイ経由で NAS/FTP サーバーをマウントできますか?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

いいえ、SSL VPN ゲートウェイからアクセスできるのはプライベート VLAN とサーバーのみです。 NAS/FTP ボリュームからデータをダウンロードするには、データをサーバーに移動してから、VPN 経由でリモート・ロケーションに移動する必要があります。

セキュリティー上の理由から、サービス (DNS、更新、NAS、Lockbox) を提供するサーバーへのアクセスを許可されているのは、データ・センター内に配置されているサーバーだけです。


## SSL VPN を提供するベンダーとその機能は?
{:#what-vendor-makes-ssl-vpn}
{:faq}

SSL VPN ゲートウェイは、Array Networks が提供するセキュリティー製品です。  ゲートウェイ自体は、カスタマー・ポータルからユーザーとパスワードを更新するために radius を実行します。 ユーザーを追加して、SSL VPN アクセス権限を付与する場合は、カスタマー・ポータル内で新規ユーザーを作成し、SSL VPN 許可を有効にします。


## SSL VPN と PPTP VPN の違いは?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL VPN** では、ユーザーはリモート・デスクトップから {{site.data.keyword.BluSoftlayer_notm}} プライベート・ネットワークへのセキュア・トンネルを作成できます。 さまざまなオペレーティング・システムと互換性があります。

**PPTP VPN** では、同じセキュア・トンネルを使用できますが、ユーザーのデスクトップまたは専用デバイスで特殊なクライアント・ソフトウェアを使用して接続します。 ただし、PPTP は非推奨になりました。詳しくは、[PPTP VPN の非推奨](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)を参照してください。

## PPTP VPN にユーザーを追加できないのはなぜですか?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP は非推奨になりました。詳しくは、[PPTP VPN の非推奨](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)を参照してください。

## カスタマー・ポータル内でユーザーの VPN 管理状況に使用可能なカテゴリーは何ですか?
{:#what-are-available-categories-vpn-management}
{:faq}

顧客状況カテゴリーには、ユーザーが更新可能なものと、自動的に表示されるものがあります。 以下のような状況があります。

* **アクティブ** - ユーザーは、アカウント管理者が設定した許可に基づいて、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) と VPN にアクセスできます。 この状況はいつでも手動で選択/変更できます。
* **無効** - ユーザーのアカウントでは、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) と VPN を含め、どの許可またはサブスクリプションにもアクセスできません。 アカウントに対して別のユーザーが無効にした場合、この状況はいつでも手動で選択/変更できます。
* **VPN のみ** - ユーザーは VPN 接続にのみアクセスでき、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) にはアクセスできません。 この状況はいつでも手動で選択/変更できます。
* **非アクティブ** - ユーザーは、最近 60 日間、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) または VPN を利用していません。 これはシステム生成の状況です。
* **取り消し保留** - アカウントの管理者がこのユーザーを取り消し、取り消しは現在処理中です。 これはシステム生成の状況です。

## SSL VPN はどのようにセットアップしますか?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

詳しくは、[SSL VPN への接続 - Windows 7 以上](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7)を参照してください。



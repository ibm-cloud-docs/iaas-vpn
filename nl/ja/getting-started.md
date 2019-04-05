---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, IBM Cloud VPN, user account

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 仮想プライベート・ネットワーキング (VPN) の概要
{:#gettingstarted-with-virtual-private-networking}

## IBM Cloud VPN とは?
{:#what-is-ibmcloud-vpn}


ユーザーは、VPN アクセスを使用することで、すべてのサーバーを IBM Cloud プライベート・ネットワーク経由でセキュアにリモート管理できます。 自分のいる場所からプライベート・ネットワークに VPN で接続すれば、暗号化された VPN トンネルを使用したアウト・オブ・バンド管理や、サーバー・レスキューが可能になります。 VPN アクセスを使用すれば、以下を行うことができます。

* SSL または IPSec によってプライベート・ネットワークへの VPN 接続を確立する
* SSH または RDP によって、プライベート IP アドレス 10.x.x.x を使用してサーバーにアクセスする
* さらなるサーバー管理やレスキューのニーズに対応するためにサーバーの IPMI IP アドレスに接続する

**[発表](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)で説明したとおり、PPTP VPN サービスは、2018 年 6 月 12 日より、非推奨になっています。**{:deprecated}

サービスによってはプライベート・ネットワークを使用したアクセスが必要となります。VPN はプライベート・ネットワーク・アクセスを可能にする 1 つの方法です。 VPN は、プライベート・ネットワークにログインし、作業を行い、ログアウトする必要がある場合に使用することをお勧めします。 多くの場合、このようなアクセスは、例えばサーバーの KVM にアクセスするために必要となります。

アカウントごとに VPN アクセス権限を付与できます。また、アクセス先とすべきサブネットに関して各アカウントを制限できます。 VPN にログインするには、VPN アクセスを有効にして VPN パスワードを作成しておく必要があります。

## 各ユーザーの VPN アクセスを有効にする
{:#enable-user-vpn-access}

最初に、VPN アクセスを必要とする各アカウントで VPN アクセスを有効にする必要があります。 各アカウント (チームのマスター・アカウントを含む) は、VPN アクセスを**無効**にした状態で開始します。 VPN アクセスを有効にするには、以下の手順に従います。

1. [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で**「アカウント」->「VPN アクセス (VPN Access)」**に移動します。
* そこに、使用可能な各 VPN ユーザーの行があり、**「VPN アクセス (VPN Access)」**列の下にリンクがあります。
* ユーザーの VPN アクセスがまだ有効になっていない場合、このリンクは「なし」と表記されています。
* ユーザーの VPN アクセス・リンクが**「SSL」**と表記されている場合、そのユーザーの VPN アクセスは既に有効になっています。

![Softlayer ポータル VPN アクセス・テーブル](images/vpnaccess01.png)

1. 特定のユーザーに許可されている VPN アクセス・タイプを有効にしたり変更したりするには、**「VPN アクセス (VPN Access)」**列の下にあるリンクをクリックします。
* 次のページで、各ユーザーに適している VPN アクセス・タイプを有効にできます。  

![VPN アクセス・タイプをユーザーに割り当てる](images/vpntype01.png)

## VPN パスワードの設定
{:#set-vpn-password}

次のステップは VPN パスワードを作成する作業です。 各ユーザーは[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で自分の VPN パスワードを作成したり更新したりできます。 これを行うには、右上にある自分の名前を選択します。そうすると、**「プロファイルの編集 (Edit profile)」**ページが表示されます。 また、**「アカウント」->「ユーザー」**を選択して自分のユーザー名を選ぶこともできます。

      注: 現在、このリンクは「マスター・ユーザー (Master User)」と表記されています。 このリンクの表記はサブユーザーに対しては自身の名前になります。

**「ユーザー・プロファイルの編集 (Edit User Profile)」**ページでスクロールダウンして、VPN パスワードを初期設定または更新します。

![プロファイルの VPN パスワード・フィールドの編集](images/vpnpasswordfields.png)

## VPN にログイン
{:#login-to-the-vpn}

VPN アクセスが確立されたため、ログインできます。

1. SSL VPN にログインするには、[vpn.softlayer.com](https://vpn.softlayer.com/) にアクセスして任意のログイン・ポイントを選択します。 任意の VPN アクセス・ポイントを使用できます。すべてのデータ・センターにおいてプライベート・ネットワークに対する同じアクセス許可が付与されます。
* あるロケーションにログインするのが困難な場合は、別のロケーションを試します。
* あるいは、スタンドアロン・クライアント SSL VPN を使用してログインできます。

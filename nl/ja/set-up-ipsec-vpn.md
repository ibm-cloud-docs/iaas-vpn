---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: IPSec VPN, IP address, IP traffic

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# IPSec VPN のセットアップ
{:#setup-ipsec-vpn}

## IPSec VPN とは?
{:#what-is-ipsec-vpn}

IPSec は、トンネル・モード (暗号化されたサイト間ネットワークを提供) を使用して 2 つのロケーション間でのすべての IP トラフィックを認証および暗号化するように設計された、一組のプロトコルです。 そのままであれば非セキュアと見なされるネットワークを経由してトラステッド・データを渡すことができます。   IPSec の一般情報については、[参照資料](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)をご覧ください。


IBM Cloud の VPN アクセスにより、ユーザーは、リモート側から、IBM Cloud のプライベート・ネットワーク経由で安全に、すべてのサーバーを管理できます。  お客様のロケーションからプライベート・ネットワークへの VPN 接続により、暗号化された VPN トンネル経由でのアウト・オブ・バンド管理とサーバー・レスキューが可能になります。  VPN アクセスを使用すれば、以下を行うことができます。

   * SSL または IPSEC を使用してプライベート・ネットワークへの VPN 接続を確立する
   * SSH または RDP を使用してプライベート IP アドレス 10.x.x.x でサーバーにアクセスする
   * さらなるサーバー管理やレスキューのニーズに対応するためにサーバーの IPMI IP アドレスに接続する

IPSec サービスは、環境の管理用にお客様に提供されています。 実動ワークロード用には推奨されません。


## IPSec 接続のセットアップ
{:#setup-ipsec-connection}

### ネゴシエーション・パラメーター
{:#setup-ipsec-vpn-negotiation-parameters}
![ネゴシエーション・パラメーター](images/IPSec_VPN.png)

IPSec VPN のリモート・サイドについて、以下の情報を把握しておく必要があります。
- VPN エンドポイントの静的 IP アドレス
- 事前共有鍵 (パスワード)
- 暗号化アルゴリズム (DES、3DES、AES128、AES192、AES256)
- 認証 (MD5、SHA1、SHA256、フェーズ 1 および 2 の場合)
- Diffie-Hellman グループ (フェーズ 1 および 2 の場合)
- Perfect Forward Secrecy (PFS) が使用されているかどうか
- Keylife Time (フェーズ 1 および 2 の場合) - **注:** 弊社システムではこの値を秒単位で計測します。

この情報が使用可能になったら、VPN 接続の基本ネゴシエーション・パラメーターを構成することができます。

### 保護されたネットワーク
{:#setup-ipsec-vpn-protected-networks}

VPN 接続プロパティーでは、トンネルのリモート・エンドのネットワークと、トンネルのローカル・ネットワークを定義する必要があります。 「保護されたカスタマー (リモート) サブネット (Protected Customer (Remote) Subnet)」で、IPSec トンネルのリモート (非 IBM) エンドのプライベート IP アドレス・スペースを CIDR 表記で入力してください。

<span style="text-decoration: underline">例:</span> トンネルのリモート・エンドのネットワークが単一サブネット 10.0.0.0 とネットマスク 255.255.255.0 を使用している場合は、IP アドレス 10.0.0.0 / CIDR 24 を「保護されたカスタマー (リモート) サブネット」セクションに入力します。

### ネットワーク・アドレス変換 (NAT)
{:#setup-ipsec-vpn-nat}

IPSec VPN では、VPN 接続の他のエンド上のリモート・サブネットにトラフィックを経路指定する、{{site.data.keyword.BluSoftlayer_notm}} ネットワーク上のプライベート IP アドレスを定義することもできます。  これにより、フル・インターネット・アクセスに対してリモート・ロケーションを公開することなく、プライベート・インターネットのトラフィックを、VPN の背後にあるマシンの内部 IP アドレスのいずれかに転送することが可能になります。  

### ネットワーク・アドレス変換/割り当て済み静的 NAT サブネット
{:#setup-ipsec-vpn-nat-static-subnets}

静的 NAT エントリーを使用してリモート VPN IP を構成するには、以下のようにします。 

 * 赤い矢印を選択して、**「割り当て済み静的 NAT サブネット (Assigned Static NAT subnets)」**セクションのサブネット・リストを表示します。 サブネット内の各 IP が表示されます。  
 * VPN 接続のリモート・エンドの IP を**「カスタマー IP (Customer IP)」**列の下に入力し、マッピングの名前を**「名前」**列の下に入力します。  
 * **「コンテキスト・アドレス変換の追加/変更 (Add/Modify Context Address Translations)」**と**「構成の適用 (Apply Configurations)」**を選択して、構成を保存および適用します。
 
この操作により、静的 1 対 1 ネットワーク変換がリターン・トラフィック用にセットアップされます。この変換は、IBM Cloud VPN コンセントレーターの背後にあるホストが、リモート VPN ピアの背後にあるホストと通信するために使用します。 例えば、IP 10.1.255.92 のトラフィックはすべて、お客様の IP 192.168.10.15 に変換され、転送されます。 この転送により、IBM Cloud サーバー上の追加の経路エントリーが不要になります。

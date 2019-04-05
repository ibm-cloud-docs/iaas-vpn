---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# PPTP VPN の非推奨
{:#pptp-vpn-deprecation}

PPTP VPN は 2018 年 6 月 12 日より非推奨になっており、お客様に対して提供されなくなりました。関心をお寄せいただきありがとうございました。代わりに利用可能なものについては後述します。

## VPN とは?
{:#pptp-vpn-deprecation-what-is-vpn}
ユーザーは、VPN アクセスを使用することで、すべてのサーバーを IBM Cloud プライベート・ネットワーク経由でセキュアにリモート管理できます。 自分のいる場所からプライベート・ネットワークに VPN で接続すれば、暗号化された VPN トンネルを使用したアウト・オブ・バンド管理や、サーバー・レスキューが可能になります。 VPN アクセスを使用すれば、以下を行うことができます。

* SSL、**PPTP**、または IPSec によってプライベート・ネットワークへの VPN 接続を確立する
* SSH または RDP によって、プライベート IP アドレス 10.x.x.x を使用してサーバーにアクセスする
* さらなるサーバー管理やレスキューのニーズに対応するためにサーバーの IPMI IP アドレスに接続する

## PPTP は非推奨
{:#pptp-deprecation-vpn}
他の VPN オプションがよりセキュアで多目的になるにつれて、PPTP のニーズが減少しています。{{site.data.keyword.BluSoftlayer_notm}} には、SSL や IPSec など、PPTP よりも高度で保護されたいくつかのオプションがあります。

**このような理由から、2018 年 6 月 12 日以降、{{site.data.keyword.BluSoftlayer_notm}} は PPTP を提供しなくなりました。**{:important}


## よくある質問
{:#pptp-vpn-deprecation-faq}

**Q: なぜ PPTP は非推奨になったのですか?**

**A:** 最高品質の保護を提供するために、{{site.data.keyword.BluSoftlayer_notm}} は PPTP の使用を中止しました。{{site.data.keyword.BluSoftlayer_notm}} は、お客様のプライバシーとデータのセキュリティーが最も重要であるという約束を守ることを望んでいます。 

**Q: 他の VPN アクセス・タイプは、PPTP 以外にどのようなものがありますか?**

**A:** {{site.data.keyword.BluSoftlayer_notm}} には、単純な構成のみを必要とするいくつかのオプションが用意されています。
  1. SSL VPN は、ブラウザーからプライベート・ネットワークに直接接続するクイック・アクセス接続です。 SSL VPN は、Windows XP 以上 (ActiveX を使用)、Fedora、Ubuntu、および Mac OSX に対応しています。 単一の URL で当社のプライベート・ネットワークにグローバルにアクセスできます。その際に、最寄りの VPN エンドポイントを選択できます。 このオプションの概要について詳しくは、[SSL VPN 接続のセットアップ](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections)を参照してください。
  2. IPSec は、2 つのロケーション間でのすべての IP トラフィックを認証および暗号化するように設計された、一組のプロトコルです。 そのままであれば非セキュアと見なされるネットワークを経由してトラステッド・データを渡すことができます。 IPSec の一般情報については、[IPSec VPN のセットアップ](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn)、および他の[参照資料](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)を参照して、このサービスの使用を開始してください。 

**Q: ビジネス慣行が PPTP を必要とする場合はどうなりますか?**

**A:** ビジネス・ニーズに応じて PPTP が必要な場合は、いくつかのオプションを使用できます。 **すべての可能なオプションがここに網羅されているわけではありません。 以下のオプションでは、両方のエンドポイントの完全な構成が必要であることに注意してください。 これらのオプションの構成はお客様にしていただきます。**
  1. Virtual Router Appliance。 Virtual Router Appliance は Vyatta とも呼ばれ、環境のゲートウェイとルーターとして機能します。 これは、サブネットで構成されるゾーンを含みます。 ファイアウォール・ルールは、相互に通信するためにゾーン間で設定されます。 他のゾーンと通信する必要のないゾーンでは、すべてのパケットがドロップされるため、ファイアウォール・ルールは必要ありません。 このサービスの概要については、[Virtual Router Appliance の概要](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance)を参照してください。 
  2. FSA ファイアウォール。 FortiGate Security Appliance (FSA) 10 Gbps は、パブリックおよびプライベートの両方のネットワークに対して複数の VLAN のトラフィックを保護するように構成できるハードウェア・ファイアウォールです。 カスタマー・ポータルでは、「複数 VLAN ファイアウォール」と呼ばれています。 このサービスの概要について詳しくは、[FSA 10 Gbps の概要](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps)を参照してください。 
 
上述のオプションは、サービスが {{site.data.keyword.BluSoftlayer_notm}} によって提供されなくなった後、ビジネス・ニーズに PPTP が必要な場合に、検討する価値を持つ可能性のあるものです。ご利用ありがとうございました。{:note}

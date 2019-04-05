---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# SSL VPN の使用
{:#use-ssl-vpn}

1. カスタマー・ポータルでナビゲーション・メニューから**「サポート」>「SSL VPN ログイン (SSL VPN Login)」**を選択して**「SSL VPN ログイン (SSL VPN Login)」**リンクにナビゲートし、資格情報を入力します。
2. タスクバーに「A」が表示されていれば、SSL VPN トンネルが確立されています。
3. これで完了です。現在、プライベート VLAN にログインしています。

## 接続後の操作
{:#now-im-connected-what-do-i-do}

1. SSH または RDC (端末サービス) を使用して、ご使用のサーバーのサーバー管理用プライベート IP アドレス (10.x.x.x) に接続します。
2. リモート・コンソール/リブート機能を使用するには、SuperMicro ソフトウェアを使用して IPMI 2.0 カードに接続します。ダウンロード手順については、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) を参照してください。
3. ドライブをサーバーにマップ (Windows) したり、ドライブをサーバーにマウント (Red Hat) したりできます。

## ヒント
{:#ssl-vpn-tips-tricks}

1. IPMI IP とプライベート IP は 1 桁ずれています。これらの IP を混同しないでください。
2. IPMI カードへの接続に SSH も RDC も使用できません。ソフトウェアを使用する必要があります。
3. ご使用の IPMI IP およびプライベート IP はハードウェア・セクションの**「サーバー」**の下にあります。
4. IPMI カードはプライベート IP インターフェースを「listen」し、IPMI トラフィックを IPMI カードにリダイレクトします。

## 製品固有の IPMI の説明
{:#product-specific-impi-instructions}

* CIFS 共有での IPMI の使用について詳しくは、[ベアメタル・サーバーへの ISO のマウント](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-)を参照してください。
* VMWare での IPMI の使用について詳しくは、[リモート・コンソールおよび仮想メディアを使用した VMware vSphere ESXi のインストール](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi)を参照してください。

* IBM POWER ハードウェアでの IPMI の使用について詳しくは、[IPMItool のインストール](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm)を参照してください。

**警告:**

`eth0` (プライベート・ネットワーク・インターフェース) を使用不可にすると、モニター、リモート・コンソール、リモート・リブートなどを含むすべての IPMI 機能が失われます。 プライベート・インターフェースへのアクセスをロックしたい場合は、「IP テーブル (IP Tables)」や「サーバー・ファイアウォール (Server Firewall)」に入力できる許可 IP アドレスのリストを参照してください。

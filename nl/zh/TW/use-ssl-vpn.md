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

# 使用 SSL VPN
{:#use-ssl-vpn}

1. 從「導覽」功能表中選取**支援 > SSL VPN 登入**，以導覽至「客戶入口網站」的 **SSL VPN 登入**鏈結，然後輸入您的認證
2. 當您在作業列中看到 "A" 時，即已建立 SSL VPN 通道。
3. 恭喜 - 您現在位於專用 VLAN。

## 現在我已連線...我要做什麼？
{:#now-im-connected-what-do-i-do}

1. 使用 SSH 或 RDC（終端機服務）來連接至伺服器的專用 IP 位址 (10.x.x.x) ，以進行伺服器管理。
2. 若要利用遠端主控台或重新開機功能，請透過 SuperMicro 軟體連接至您的 IPMI 2.0 卡－如需下載指示，請參閱[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/)。
3. 您可以將磁碟機對映至伺服器 (Windows)，也可以將磁碟機裝載至伺服器 (Red Hat)。

## 要訣和技巧
{:#ssl-vpn-tips-tricks}

1. 您的 IPMI IP 及「專用 IP」有一個數字不同，別搞混了。
2. 您無法使用 SSH 或 RDC 來連接至 IPMI 卡，您必須使用軟體。
3. 您的 IPMI IP 及「專用 IP」位於硬體區段的每一個**伺服器**下。
4. 您的 IPMI 卡會在專用 IP 介面上「接聽」，並將 IPMI 資料流量重新導向至 IPMI 卡。

## 產品特有的 IPMI 指示
{:#product-specific-impi-instructions}

* 如需在 CIFS 共用上使用 IPMI 的相關資訊，請參閱[在裸機伺服器上裝載 ISO](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-)。
* 如需使用 IPMI 搭配 VMWare 的相關資訊，請參閱[透過遠端主控台及虛擬媒體安裝 VMware vSphere ESXi](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi)。

* 如需使用 IPMI 搭配 IBM POWER 硬體的相關資訊，請參閱[安裝 IPMItool](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm)。

**警告：**

如果您停用 `eth0`（它是專用網路介面），您將會遺失所有 IPMI 功能，包括監視、遠端主控台、遠端重新開機等等。如果您要鎖定專用介面的存取權，請參閱可讓您輸入到「IP 表格」或「伺服器防火牆」的容許 IP 位址清單。

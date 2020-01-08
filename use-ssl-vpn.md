---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-12-02"

keywords: Use SSL VPN navigate, private IP address, private VLAN, IaaS VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:term: .term}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}
{:generic: data-hd-programlang="generic"}
{:download: .download}
{:DomainName: data-hd-keyref="DomainName"}
{:term: .term}

# Using an SSL VPN
{:#using-ssl-vpn}
SSL VPN establishes a VPN connection between your system and the {{site.data.keyword.cloud}} private network by using client software to adjust your system's network settings to send select traffic to the private network. Depending on the operating system that you're using, you can access SSL VPN in a few different ways. The easiest way to access SSL VPN is to select a VPN endpoint directly from your browser and follow the plug-in installation prompts. However, if you come across problems when you use the browser-based solution, so you might need to review operating system-specific instructions.
{:shortdesc}

Follow these steps to connect to an SSL VPN endpoint:

1. For supported operating systems, click any one of the available [SSL VPN connection locations](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints).
2. Follow the prompts to accept use of the SSL VPN client software.
3. When prompted, enter your VPN login credentials.

## Next steps
{:#now-im-connected-what-do-i-do}

1. Use SSH or remote desktop to connect to your server's primary private IP address.
2. Use remote management to [mount an ISO to your server](/docs/bare-metal?topic=bare-metal-bm-mount-iso).
3. Use remote management functions that aren't provided by the [{{site.data.keyword.cloud}} console](http://{DomainName}/){:external}. To do so, access your bare metal or virtual server's respective **KVM Console** by selecting **Classic Infrastructure > Devices > (your server) > Remote Management > Actions > KVM Console**.

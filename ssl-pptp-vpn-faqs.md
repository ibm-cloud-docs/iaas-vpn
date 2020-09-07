---

copyright:
  years: 1994, 2020
lastupdated: "2020-02-21"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}
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

# SSL VPN FAQs
{: #vpn-ssl-faq}

These FAQs provide answers to common questions about SSL VPNs.
{:shortdesc}

## What is {{site.data.keyword.cloud_notm}} VPN?
{: #what-is-ibm-cloud-vpn}
{: faq}
{: support}

{{site.data.keyword.cloud}} VPN access is designed to allow users to remotely manage all servers securely over the {{site.data.keyword.cloud_notm}} private network. A VPN connection from your location to the private network allows for out-of-band management and server rescue through an encrypted VPN tunnel. VPN tunnels can be created to any IBM Cloud data center or PoP providing geographic redundancy.

With VPN access, you can:

* Establish a VPN connection to the private network by using SSL or IPsec
* Access your server through its private 10.x.x.x IP address by using SSH or RDP
* Connect to your server’s IPMI IP address for server management or rescue needs.

## What if I cannot connect to the SSL or IPsec VPN endpoint of my choice?
{: #what-if-i-cannot-connect-to-vpn-endpoint}
{: faq}
{: support}

Geographic redundancy exists to allow access into your private network from anywhere in the world that you choose to connect from.  If one location does not connect, you can open an IBM Support ticket for more information, or you can use a different data center during the interruption.

## Does the SSL VPN also perform IPsec or other VPN protocols?
{: #does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{: faq}
{: support}

Currently, the SSL VPN gateway uses a browser-based SSL VPN plug-in or a proprietary client for creating connections. We continue to bring more VPN connectivity options to the private network. The SSL VPN was selected for ease of use and compatibility.

## Can I mount the NAS/FTP server from my remote location over the SSL VPN gateway?
{: #can-i-mount-nas-ftp-remotely}
{: faq}
{: support}

No. You have access to your private VLAN and servers only from the SSL VPN gateway. If you want to download data from your NAS/FTP volume, you must move the data to your server then out through the VPN to the remote location.

For security reasons, only servers that are located inside the data center are allowed access to the servers, which provide services (DNS, Update, NAS, Lockbox).

## What vendor makes the SSL VPN and how does it work?
{: #what-vendor-makes-ssl-vpn}
{: faq}
{: support}

Our SSL VPN gateway is a security product from Array Networks. The gateway itself runs radius to update users and passwords from our customer portal. If you want to add users and give them SSL VPN access, create a new user inside the customer portal and enable SSL VPN permissions.

## What are the available categories for a user's VPN management status within the customer portal?
{: #what-are-available-categories-vpn-management}
{: faq}
{: support}

* **Active** - The user has access to the [{{site.data.keyword.cloud_notm}} infrastructure customer portal](https://control.softlayer.com/){:external} and VPN based on permissions set by the account administrator. This status can be manually selected and changed at any time.
* **Disabled** - The user does not have access to any permissions or subscriptions on the account, including [customer portal](https://control.softlayer.com/){:external} and VPN. If set to disabled by another user on the account, this status can be manually selected and changed at any time.
* **VPN Only** - The user has access to only VPN connectivity and cannot access the [customer portal](https://control.softlayer.com/){:external}. This status can be manually selected or changed at any time.
* **Inactive** - The user hasn't used the [customer portal](https://control.softlayer.com/){:external} or VPN in the last 60 days (system-generated status).
* **cancel_pending** - An administrator on the account cancelled this user and the cancellation is being processed. (system-generated status).

## How do I set up SSL VPN?
{: #how-do-i-set-up-ssl-vpn}
{: faq}
{: support}

SSL VPN is a quick-access connection that connects you to our private network directly from a browser. For detailed instructions on how to set up SSL VPN, see [Connecting to SSL VPN (Windows 7 and higher)](/docs/iaas-vpn?topic=iaas-vpn-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).

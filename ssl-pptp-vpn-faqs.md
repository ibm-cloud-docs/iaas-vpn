---

copyright:
  years: 1994, 2021
lastupdated: "2021-10-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# SSL VPN FAQs
{: #vpn-ssl-faq}

These FAQs provide answers to common questions about SSL VPNs.
{: shortdesc}

## What is {{site.data.keyword.cloud_notm}} VPN?
{: #what-is-ibm-cloud-vpn}
{: faq}
{: support}

{{site.data.keyword.cloud}} VPN access is designed to allow users to remotely manage all servers securely over the {{site.data.keyword.cloud_notm}} private network. A VPN connection from your location to the private network allows for out-of-band management and server rescue through an encrypted VPN tunnel. VPN tunnels can be created to any {{site.data.keyword.cloud_notm}} data center or PoP providing geographic redundancy.

With VPN access, you can:

* Establish a VPN connection to the private network by using SSL or IPsec
* Access your server through its private `10.x.x.x` IP address by using SSH or RDP
* Connect to your server’s IPMI IP address for server management or rescue needs.

Our SSL VPN gateway is a security product from Array Networks. The gateway itself runs radius to update users and passwords from our customer portal.

## What if I cannot connect to the SSL or IPsec VPN endpoint of my choice?
{: #what-if-i-cannot-connect-to-vpn-endpoint}
{: faq}
{: support}

Geographic redundancy exists to allow access into your private network from anywhere in the world that you choose to connect from.  If one location does not connect, you can open an [IBM Support case](https://cloud.ibm.com/unifiedsupport/cases/form){: external} for more information, or you can use a different data center during the interruption.

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

## How does VPN access work?
{: #what-vendor-makes-ssl-vpn}
{: faq}
{: support}

First, an account administrator must enable SSL VPN permissions for users. As a user, you can log in to the VPN through [the web interface]( https://www.ibm.com/cloud/vpn-access) or use a [stand-alone VPN client](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients) for Linux, MacOS, or Windows. For more information, see [Logging in to the VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started#login-to-the-vpn).

## What are the available categories for a user's VPN management status within the customer portal?
{: #what-are-available-categories-vpn-management}
{: faq}
{: support}

* **Active** - The user has access to the [{{site.data.keyword.cloud_notm}} infrastructure customer portal](https://control.softlayer.com/){: external} and VPN based on permissions set by the account administrator. This status can be manually selected and changed at any time.
* **Disabled** - The user does not have access to any permissions or subscriptions on the account, including [customer portal](https://control.softlayer.com/){: external} and VPN. If set to disabled by another user on the account, this status can be manually selected and changed at any time.
* **VPN Only** - The user has access to only VPN connectivity and cannot access the [customer portal](https://control.softlayer.com/){: external}. This status can be manually selected or changed at any time.
* **Inactive** - The user hasn't used the [customer portal](https://control.softlayer.com/){: external} or VPN in the last 60 days (system-generated status).
* **cancel_pending** - An administrator on the account cancelled this user and the cancellation is being processed. (system-generated status).

## How do I set up SSL VPN?
{: #how-do-i-set-up-ssl-vpn}
{: faq}
{: support}

SSL VPN is a quick-access connection that connects you to our private network directly for non-production use. For detailed instructions about setting up SSL VPN, see [Getting started with SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

## Why isn't auto-disconnect working?
{: #auto-disconnect}
{: faq}
{: support}

Auto-disconnect is working as expected because SSL VPN is designed to manage classic servers, but not for production use. There is a check against idle clients and the token is terminated if time is up.

## Are there open-source alternatives to SSL VPN?
{: #open-source-alter}
{: faq}
{: support}

Yes, you can set up [WireGuard](https://www.wireguard.com/){: external} or [OpenVPN](https://openvpn.net/){: external} servers on {{site.data.keyword.cloud_notm}}, and build your own VPN tunnels from on-premises to {{site.data.keyword.cloud_notm}}.

## Why do I get redirected by the browser to install MotionPro client when it's already installed on my Mac?
{: #redirect-install}
{: faq}
{: support}

This is a known issue with the combination of the OSX Operating System (macOS BigSur 11.4) and the Firefox browser (89.0.2 64-bits). To avoid this issue, try to launch the MotionPro client from your local system rather than accessing one of the VPN endpoints from a browser.

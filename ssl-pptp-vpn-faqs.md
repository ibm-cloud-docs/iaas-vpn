---

copyright:
  years: 1994, 2025
lastupdated: "2025-07-09"

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

* Establish a VPN connection to the private network by using SSL
* Access your server through its private `10.x.x.x` IP address by using SSH or RDP
* Connect to your server’s IPMI IP address for server management or rescue needs.

Our SSL VPN gateway is a security product from Array Networks. The gateway itself runs radius to update users and passwords from our customer portal.

## What if I cannot connect to the SSL VPN endpoint of my choice?
{: #what-if-i-cannot-connect-to-vpn-endpoint}
{: faq}
{: support}

Geographic redundancy exists to allow access into your private network from anywhere in the world that you choose to connect from. If one location doesn't connect, you can use a different data center during the interruption. If multiple locations are failing to connect, visit our Troubleshooting section.

## Does the SSL VPN also perform other VPN protocols?
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

First, an account administrator must enable SSL VPN permissions for users. As a user, you can log in to the VPN through [the web interface](https://www.ibm.com/products/vpn-access) or use a [stand-alone VPN client](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients) for Linux, MacOS, or Windows. For more information, see [Logging in to the VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started#login-to-the-vpn).

## What are the available categories for a user's VPN management status within the customer portal?
{: #what-are-available-categories-vpn-management}
{: faq}
{: support}

* **Active** - The user has access to the [{{site.data.keyword.cloud_notm}} infrastructure customer portal](https://control.softlayer.com/){: external} and VPN based on permissions set by the account administrator. This status can be manually selected and changed at any time.
* **Disabled** - The user does not have access to any permissions or subscriptions on the account, including [customer portal](https://control.softlayer.com/){: external} and VPN. If set to disabled by another user on the account, this status can be manually selected and changed at any time.
* **VPN Only** - The user has access to only VPN connectivity and cannot access the [customer portal](https://control.softlayer.com/){: external}. This status can be manually selected or changed at any time.

## How do I set up SSL VPN?
{: #how-do-i-set-up-ssl-vpn}
{: faq}
{: support}

SSL VPN is a quick-access connection that connects you to our private network directly for non-production use. For detailed instructions about setting up SSL VPN, see [Getting started with SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

## Are there open-source alternatives to SSL VPN?
{: #open-source-alter}
{: faq}
{: support}

Yes, you can set up [WireGuard](https://www.wireguard.com/){: external} or [OpenVPN](https://openvpn.net/){: external} servers on {{site.data.keyword.cloud_notm}}, and build your own VPN tunnels from on-premises to {{site.data.keyword.cloud_notm}}.

## What is the process of installing MotionPro on Windows, Mac, or Linux?
{: #os-install}
{: faq}
{: support}

1. Uninstall your current version of MotionPro (if applicable).
1. Restart your system.
1. Download and install the latest version of MotionPro.

## How do I request SSL-VPN logs?
{: #faq-ssl-cert-5}
{: faq}
{: support}

Requesting SSL-VPN audit logs requires that you open a support case to ensure proper protocol, security, and policies are followed. For security reasons, only the primary account holder can make the request for SSL-VPN audit logs. VPN logs are not available in real time as there can be a delay in availability. Due to the sensitive nature of the content, sometimes not all information can be shared. Please provide the following items for the request:

1) VPN username or IP address
2) Date (range is preferable)
3) Suggested times including time-zone
4) VPN endpoint (if known)

## What ciphers are supported for SSL VPN?
{: #faq-supported-ciphers}
{: faq}
{: support}

Connections to SSL VPN use the following ciphers: AES256-SHA, AES128-SHA.

---

copyright:
  years: 1994, 2019
lastupdated: "2019-08-12"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# FAQs
{:#vpn-faq}

## What is {{site.data.keyword.cloud_notm}} VPN?
{:#what-is-ibm-cloud-vpn}
{:faq}

{{site.data.keyword.cloud}} VPN access is designed to allow users to remotely manage all servers securely over the {{site.data.keyword.cloud_notm}} private network.  A VPN connection from your location to the private network allows for out-of-band management and server rescue through an encrypted VPN tunnel. With VPN access, you can:

* Establish a VPN connection to the private network using SSL or IPSEC
* Access your server via its private 10.x.x.x IP address using SSH or RDP
* Connect to your server’s IPMI IP address for additional server management or rescue needs.


## Does the SSL VPN also perform PPTP, IPSEC or other VPN protocols?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Currently the SSL VPN gateway uses a browser-based SSL VPN plugin or a proprietary client for creating connections. We will continue to bring more VPN connectivity options to the private network. The SSL VPN was selected for ease of use and compatibility. PPTP is deprecated. See [PPTP VPN Deprecation](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) for more information.



## Can I mount the NAS/FTP server from my remote location over the SSL VPN gateway?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

No...you only have access to your private VLAN and servers from the SSL VPN gateway. If you wish to download data from your NAS/FTP volume, you must move the data to your server then out through the VPN to the remote location.

For security reasons, only servers located inside the datacenter are allowed access to the servers providing services (DNS, Update, NAS, Lockbox).


## What vendor makes the SSL VPN and how does it work?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Our SSL VPN gateway is a security product from Array Networks.  The gateway itself runs radius to update users and passwords from our customer portal. If you wish to add users and give them SSL VPN access, create a new user inside the customer portal and enable SSL VPN permissions.


## What is the difference between SSL and PPTP VPN?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL VPN** allows a user to create a secure tunnel from the remote desktop to the {{site.data.keyword.BluSoftlayer_notm}} Private Network. It is compatible with a variety of operating systems.

**PPTP VPN** allows the same secure tunnel but connects using specialized client software on a user's desktop or dedicated device. However, PPTP is deprecated. See [PPTP VPN Deprecation](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) for more information.

## Why am I unable to add additional users for PPTP VPN?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP is deprecated. See [PPTP VPN Deprecation](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) for more information.

## What are the available categories for a user's VPN management status within the customer portal?
{:#what-are-available-categories-vpn-management}
{:faq}

Customer status categories include those that are able to be updated by a user and those that may appear automatically. They include:

* **Active** - The user has access to the [{{site.data.keyword.cloud_notm}} infrastructure customer portal](https://control.softlayer.com/){:external} and VPN based on permissions set by the account administrator. This status may be manually selected or changed at any time.
* **Disabled** - The user does not have access to any permissions or subscriptions on the account, including [customer portal](https://control.softlayer.com/){:external} and VPN. If set to disabled by another user on the account, this status may be manually selected and/or changed at any time.
* **VPN Only** - The user only has access to VPN connectivity and may not access the [customer portal](https://control.softlayer.com/){:external}. This status may be manually selected or changed at any time.
* **Inactive** - The user has not utilized the [customer portal](https://control.softlayer.com/){:external} or VPN in the last 60 days. This is a system-generated status.
* **cancel_pending** - An administrator on the account has canceled this user and the cancellation is currently being processed. This status is a system-generated status.

## How do I set up SSL VPN?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

SLL VPN is a quick-access connection that connects you to our private network directly from a browser. For detailed instructions on how to set up SSL VPN, see [Connect to SSL VPN - Windows 7 and higher](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# VPN FAQ

## What is IBM Cloud VPN?

IBM Cloud VPN access is designed to allow users to remotely manage all servers securely over the IBM Cloud private network.  A VPN connection from your location to the private network allows for out-of-band management and server rescue through an encrypted VPN tunnel. With VPN access, you can:

* Establish a VPN connection to the private network using SSL or IPSEC
* Access your server via its private 10.x.x.x IP address using SSH or RDP
* Connect to your server’s IPMI IP address for additional server management or rescue needs.


## Does the SSL VPN also perform PPTP, IPSEC or other VPN protocols?

Currently the SSL VPN gateway uses a browser-based SSL VPN plugin or a proprietary client for creating connections. We will continue to bring more VPN connectivity options to the private network. The SSL VPN was selected for ease of use and compatibility. PPTP is deprecated. See [PPTP VPN Deprecation](pptp-deprecation.html) for more information.


<a name="152"></a>
## Can I mount the NAS/FTP server from my remote location over the SSL VPN gateway?

No...you only have access to your private VLAN and servers from the SSL VPN gateway. If you wish to download data from your NAS/FTP volume, you must move the data to your server then out through the VPN to the remote location.

For security reasons, only servers located inside the datacenter are allowed access to the servers providing services (DNS, Update, NAS, Lockbox).

<a name="175"></a>
## What vendor makes the SSL VPN and how does it work?

Our SSL VPN gateway is a security product from Array Networks.  The gateway itself runs radius to update users and passwords from our Customer Portal. If you wish to add users and give them SSL VPN access, create a new user inside the customer portal and enable SSL VPN permissions.

<a name="276"></a>
## What is the difference between SSL and PPTP VPN?

**SSL VPN** allows a user to create a secure tunnel from the remote desktop to the {{site.data.keyword.BluSoftlayer_notm}} Private Network. It is compatible with a variety of operating systems.

**PPTP VPN** allows the same secure tunnel but connects using specialized client software on a user's desktop or dedicated device. However, PPTP is deprecated. See [PPTP VPN Deprecation](pptp-deprecation.html) for more information.

## When I connect to the PPTP VPN, it states "Error 691: Access was denied because the username and/or password is invalid." How do I fix this problem?

All users have the ability to connect to the PPTP VPN, but must have permission to log in through the Customer Portal.  PPTP VPN permissions are easily verified and updated quickly.  Refer to [Activate or Deactivate PPTP VPN Access](activate-a-user.html) for more information. However, PPTP is deprecated. See [PPTP VPN Deprecation](pptp-deprecation.html) for more information.


## Why am I unable to add additional users for PPTP VPN?

PPTP is deprecated. See [PPTP VPN Deprecation](pptp-deprecation.html) for more information.

## What are the available categories for a user's VPN management status within the Customer Portal?

Customer status categories include those that are able to be updated by a user and those that may appear automatically. They include:

* **Active** - The user has access to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) and VPN based on permissions set by the account administrator. This status may be manually selected or changed at any time.
* **Disabled** - The user does not have access to any permissions or subscriptions on the account, including [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) and VPN. If set to disabled by another user on the account, this status may be manually selected and/or changed at any time.
* **VPN Only** - The user only has access to VPN connectivity and may not access the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). This status may be manually selected or changed at any time.
* **Inactive** - The user has not utilized the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) or VPN in the last 60 days. This is a system-generated status.
* **cancel_pending** - An administrator on the account has canceled this user and the cancellation is currently being processed. This status is a system-generated status.

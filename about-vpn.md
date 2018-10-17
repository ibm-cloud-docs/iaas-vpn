---
copyright:
  years: 1994, 2017
lastupdated: "2018-10-16"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# About VPN

VPN access enables you to manage all servers and services associated with your account, remotely, over the IBM Cloud private network. A VPN connection from your location to the private network allows **out-of-band management and server rescue** through an encrypted VPN tunnel.

Communicating using the private network is inherently more secure. It gives you the flexibility to limit public access while still being able to manage your servers. Any user on your account can be given VPN access, which is available as SSL. VPN interactions through the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) allow for VPN access customization at the user level.

## What are some ways to use the SSL VPN?

This out-of-band secure gateway gives you access to your server over the private network. Common uses are:

* Connect to your server's private IP address (10.x.x.x) for SSH or RDC.
* Connect to your IPMI card for remote console/access/monitoring.
* Mount drives in Windows or Red Hat from home or work PC for convenience.
* Shut down public interface on database servers and manage over the private network.
* Shut down public interface while setting up the server for the first time.
* Shut down public interface during critical security updates.
* Shut down public interface during security breach and resolve the issue over the private network.

## Key Features

 * Our private network gives you a cost-free way to communicate with and manage servers. The VPN is the gateway to this private network.
 * Access points throughout the world create the best and quickest access and interaction possible. IBM Cloud currently has VPN access points in many cities.
 * Visit http://www.softlayer.com/vpn-access for a list of VPN access points to the {{site.data.keyword.BluSoftlayer_notm}} private network.

## How it Works

With VPN access, use SSL to connect with the private network and manage your server and services. 

## SSL VPN Connections

SSL VPN is a quick-access connection that connects you to our private network directly from a browser. The SSL VPN is compatible with Windows XP or higher and ActiveX, Fedora, Ubuntu, and Mac OSX. Global access to our private network is available at a single URL, which allows you to choose the nearest VPN endpoint.

## SSL VPN Subnet Limit

The SSL VPN client has a hard 64-subnet limit that it can use to populate its routing table. If your account has more than 64 subnets, make sure that you modify your SSL VPN permissions to use manual subnet assignment. If you do not, some subnets can become unreachable through the SSL VPN.

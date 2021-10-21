---

copyright:
  years: 1994, 2020
lastupdated: "2020-02-21"

keywords: IPsec VPN, IP address, IP traffic, IaaS VPN, Fedora, Windows, Linux, SSL VPN

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
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Setting up an IPsec VPN connection
{: #setup-ipsec-vpn}
{: help}
{: support}

## What is IPsec VPN?
{: #what-is-ipsec-vpn}

IPsec is a suite of protocols that are designed to authenticate and encrypt all IP traffic between two locations. It allows trusted data to pass through networks, which otherwise would be considered insecure. IPsec tunnel endpoints can be located anywhere and still provide access to your entire private network, or the networks you specify. IPsec tunnels are incompatible if you are using a zone, or cloud service endpoints.
{: shortdesc}

IBM Cloud VPN access allows users to manage all servers remotely and securely over the IBM Cloud Private network. A VPN connection from your location to the private network gives you the capability for out-of-band management and server rescue through an encrypted VPN tunnel. With VPN access, you can:

* Establish a VPN connection to the private network through SSL or IPsec.
* Access your server by using its private 10.x.x.x IP address through SSH or RDP.
* Connect to your server’s IPMI IP address for additional server management or rescue needs.

We provide the IPsec service to customers for management of their environments. It is not recommended for production workloads.

### Negotiation parameters
{: #setup-ipsec-vpn-negotiation-parameters}

![Negotiation Parameters](images/IPSec_VPN.png)

You need to know the following information for the remote side of the IPsec VPN:

- Static IP address for VPN endpoint
- Preshared key (Password)
- Encryption algorithm (DES, 3DES, AES128, AES192, AES256)
- Authentication (MD5, SHA1, SHA256, for phase 1&2)
- Diffie-Hellman Group (for phase 1&2)
- Is Perfect Forward Secrecy (PFS) used?
- Key life time (for phase 1 & 2) - **Note:** Our system measures this value in seconds!

After you have this information available, you can configure the basic negotiation parameters of the VPN connection.

### Protected networks
{: #setup-ipsec-vpn-protected-networks}

In the VPN connection properties, you must define the networks on the remote end of the tunnel and the local networks for the tunnel. In the “Protected Customer (Remote) Subnet”, enter the private IP address space in CIDR notation for the remote (Non-IBM) end of the IPsec tunnel.

For example, if your network on the remote end of the tunnel uses a single subnet `10.0.0.0` with a netmask of `255.255.255.0`, you would enter IP address `10.0.0.0 / CIDR 24` for the “Protected Customer (Remote) Subnet” section.

### Network Address Translation (NAT)
{: #setup-ipsec-vpn-nat}

With the IPsec VPN, you also are allowed to define private IP addresses on the {{site.data.keyword.BluSoftlayer_notm}} network that will route traffic to remote subnets on the other end of the VPN connection. This allows you to have private internet traffic that is forwarded to one of your internal IP addresses of a system behind your VPN, without exposing the remote location to full internet access.  

### Network Address Translation/assigned static NAT subnets
{: #setup-ipsec-vpn-nat-static-subnets}

To configure a remote VPN IP with a static NAT entry:

* Select the red arrow to display the subnet list in the **Assigned Static NAT subnets** section. Each IP in the subnet is displayed.  
* Enter the IP on the remote end of the VPN connection under the **Customer IP** column and enter a name for the mapping under the **Name** column.  
* Select the **Add/Modify Context Address Translations** and **Apply Configurations** to save and apply the configuration.

This action sets up a static one-to-one network translation for the return traffic, which is used by your hosts behind the IBM Cloud VPN concentrator to communicate with the hosts behind the remote VPN peer. For example, all traffic for IP `10.1.255.92` will be translated and forwarded to the customer's IP `192.168.10.15`. This forwarding eliminates the need for more route entries on the {{site.data.keyword.cloud_notm}} server.

---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Set Up IPSec VPN

## What is IPSec VPN?

IPSec is a suite of protocols designed to authenticate and encrypt all IP traffic between two locations, using a tunnel mode that provides an encrypted, site-to-site network. It allows trusted data to pass through networks that otherwise would be considered insecure.   For more general information regarding IPSec, refer to the [reference documents](external-reference.html).


IBM Cloud's VPN access allows users to manage all servers remotely and securely over IBM Cloud's private network.  A VPN connection from your location to the private network gives you the capability for out-of-band management and server rescue through an encrypted VPN tunnel.  With VPN access, you can:

   -Establish a VPN connection to the private network via SSL, PPTP or IPSEC
   -Access your server via its private 10.x.x.x IP address via SSH or RDP
   -Connect to your server’s IPMI IP address for additional server management or rescue needs.

We provide the IPSec service to customers for management of their environments. It is not recommended for production workloads.


## Setting up an IPSec Connection

### Negotiation Parameters
![Negotiation Parameters](images/IPSec_VPN.png)

You will need to know the following information for the remote side of the IPSec VPN:
- Static IP Address for VPN Endpoint
- Preshared Key (Password)
- Encryption Algorithm (DES, 3DES, AES128, AES192, AES256)
- Authentication (MD5, SHA1, SHA256, for phase 1&2)
- Diffie-Hellman Group (for phase 1&2)
- Is perfect Forward Secrecy (PFS) used?
- Keylife Time (for phase 1 & 2) - **NOTE:** Our system measures this value in seconds!

Once you have this information available, you can configure the basic negotiation parameters of the VPN connection.

### Protected Networks
![Protected Networks](http://14bc7.http.dal05.cdn.softlayer.net/images/protected_networks.png)

In the VPN connection properties, you must define the networks on the remote end of the tunnel as well as the local networks for the tunnel. In the “Protected Customer (Remote) Subnet”, enter the private IP address space in CIDR notation for the remote (Non-IBM) end of the IPSec tunnel.

<span style="text-decoration: underline">For example:</span>  If your network on the remote end of the tunnel uses a single subnet 10.0.0.0 with a netmask of 255.255.255.0, you would enter IP Address 10.0.0.0 / CIDR 24 for the “Protected Customer (Remote) Subnet” section.

### Network Address Translation (NAT)
![Network Address Translation](http://14bc7.http.dal05.cdn.softlayer.net/images/nat.png)

With the IPSec VPN, you also are allowed to define Private IP addresses on the {{site.data.keyword.BluSoftlayer_notm}} network that will route traffic to remote subnets on the other end of the VPN connection.  This allows you to have Private Internet traffic forwarded to one of your internal IP addresses of a machine behind your VPN, without exposing the remote location to full Internet access.  

### Network Address Translation/Assigned Static NAT Subnets

To configure a remote VPN IP with a static NAT entry: 

 * Select the red arrow to display the subnet list in the **Assigned Static NAT subnets** section. Each IP in the subnet will be displayed.  
 * Enter the IP on the remote end of the VPN connection under the **Customer IP** column and enter a name for the mapping under the **Name** column.  
 * Select the **Add/Modify Context Address Translations** and **Apply Configurations** to save and apply the configuration.
 
This action sets up a static one-to-one network translation for the return traffic, which is used by your hosts behind the IBM Cloud VPN concentrator to communicate with the hosts behind the remote VPN peer. For example, all traffic for IP 10.1.255.92 will be translated and forwarded to the customer's IP 192.168.10.15. This forwarding eliminates the need for additional route entries on the IBM Cloud server.

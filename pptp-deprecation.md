---
copyright:
  years: 2018
lastupdated: "2018-03-14"
---

# PPTP VPN Deprecation June 12, 2018

## What is IBM Cloud VPN?
VPN access enables users to manage all servers remotely and securely over the IBM Cloud private network. A VPN connection from your location to the private network allows out-of-band management and server rescue through an encrypted VPN tunnel. With VPN access, you can:

* Establish a VPN connection to the private network by SSL, **PPTP** or IPSec
* Access your server using its private 10.x.x.x IP address by SSH or RDP
* Connect to your server’s IPMI IP address for additional server management or rescue needs

## PPTP Deprecation
As other VPN options become more secure and versatile, the need for PPTP has diminished. {{site.data.keyword.BluSoftlayer_notm}} provides several other options, such as SSL or IPSec, that are more sophisticated and protective than PPTP.

## **For these reasons, {{site.data.keyword.BluSoftlayer_notm}} no longer will offer PPTP as of June 12th, 2018.**


## Frequently Asked Questions

**Q: Why is PPTP being deprecated?**

**A:** To provide the highest quality protection, {{site.data.keyword.BluSoftlayer_notm}} has decided to discontinue the use of PPTP. {{site.data.keyword.BluSoftlayer_notm}} wishes to uphold the promise to our customers that the security of their privacy and data are of the utmost importance. 

**Q: What other VPN access types are available other than PPTP?**

**A:** {{site.data.keyword.BluSoftlayer_notm}} offers several options that require only simple configuration.
  1. SSL VPN is a quick-access connection that connects you to our private network directly from a browser. The SSL VPN is compatible with Windows XP or higher and ActiveX, Fedora, Ubuntu, and Mac OSX. Global access to our private network is available at a single URL, which allows you to choose the nearest VPN endpoint. Please see [Set Up SSL VPN Connection](set-up-ssl-vpn-connections.html#set-up-ssl-vpn-connections) for more details on getting started with this option.
  2. IPSec is a suite of protocols designed to authenticate and encrypt all IP traffic between two locations. It allows trusted data to pass through networks which otherwise would be considered insecure. For more general information regarding IPSec, refer to [Set Up IPSec VPN](set-up-ipsec-vpn.html#what-is-ipsec-vpn-) and the other [reference documents](external-reference.html#external-reference-documentation) to get started using this service. 

**Q: What if my business practices require PPTP?**

**A:** Several options are available if PPTP is required for your business needs. **Not all possible options are encompassed here. Please take note that the following options require full configuration of both endpoints. The customer is responsible for the configuration of these options.**
  1. Virtual Router Appliance. The Virtual Router Appliance, also known as Vyatta, serves as a gateway and router for your environment. It contains zones consisting of subnets. Firewall rules are set in place between zones for communication with each other. For zones that do not need to communicate with other zones, no firewall rule is needed because all packets will be dropped. Please refer to [Getting Started with the Virtual Router Appliance](../virtual-router-appliance/getting-started.html) for more details on getting started with this service. 
  2. FSA Firewall. The FortiGate Security Appliance (FSA) 10Gbps is a hardware firewall that can be configured to protect traffic on multiple VLANs for both public and private networks. In the Customer Portal it is referred to as a “Multi VLAN Firewall”. Please refer to [Getting Started with FSA 10 Gbps](../fortigate-10g/getting-started.html#getting-started) for more details on getting started with this service. 
 
 **Note: The previous options are a few possibilities you can explore if PPTP is required for your business needs, after the service is no longer provided by {{site.data.keyword.BluSoftlayer_notm}}. We thank you for your business.**

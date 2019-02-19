---
copyright:
  years: 2018
lastupdated: "2018-10-17"
---

# PPTP VPN deprecation

PPTP VPN was deprecated effective June 12, 2018, and it is no longer offered to customers. Thank you for your interest. To find out about some possible alternatives, read on.

## What is VPN?
VPN access enables users to manage all servers remotely and securely over the IBM Cloud private network. A VPN connection from your location to the private network allows out-of-band management and server rescue through an encrypted VPN tunnel. With VPN access, you can:

* Establish a VPN connection to the private network by SSL, **PPTP** or IPSec
* Access your server using its private 10.x.x.x IP address by SSH or RDP
* Connect to your server’s IPMI IP address for additional server management or rescue needs

## PPTP Deprecation
As other VPN options become more secure and versatile, the need for PPTP is diminished. {{site.data.keyword.BluSoftlayer_notm}} provides several other options, such as SSL or IPSec, that are more sophisticated and protective than PPTP.

## **For these reasons, {{site.data.keyword.BluSoftlayer_notm}} no longer is offering PPTP as of June 12th, 2018.**


## Frequently Asked Questions

**Q: Why was PPTP deprecated?**

**A:** To provide the highest quality protection, {{site.data.keyword.BluSoftlayer_notm}} discontinued the use of PPTP. {{site.data.keyword.BluSoftlayer_notm}} wishes to uphold the promise to our customers that the security of their privacy and data are of the utmost importance. 

**Q: What other VPN access types are available other than PPTP?**

**A:** {{site.data.keyword.BluSoftlayer_notm}} offers several options that require only simple configuration.
  1. SSL VPN is a quick-access connection that connects you to our private network directly from a browser. The SSL VPN is compatible with Windows XP or higher and ActiveX, Fedora, Ubuntu, and Mac OSX. Global access to our private network is available at a single URL, which allows you to choose the nearest VPN endpoint. Please see [Set Up SSL VPN Connection](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) for more details on getting started with this option.
  2. IPSec is a suite of protocols designed to authenticate and encrypt all IP traffic between two locations. It allows trusted data to pass through networks which otherwise would be considered insecure. For more general information regarding IPSec, refer to [Set Up IPSec VPN](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) and the other [reference documents](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation) to get started using this service. 

**Q: What if my business practices require PPTP?**

**A:** Several options are available if PPTP is required for your business needs. **Not all possible options are encompassed here. Please take note that the following options require full configuration of both endpoints. The customer is responsible for the configuration of these options.**
  1. Virtual Router Appliance. The Virtual Router Appliance, also known as Vyatta, serves as a gateway and router for your environment. It contains zones consisting of subnets. Firewall rules are set in place between zones for communication with each other. For zones that do not need to communicate with other zones, no firewall rule is needed because all packets will be dropped. Please refer to [Getting Started with the Virtual Router Appliance](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance) for more details on getting started with this service. 
  2. FSA Firewall. The FortiGate Security Appliance (FSA) 10Gbps is a hardware firewall that can be configured to protect traffic on multiple VLANs for both public and private networks. In the Customer Portal it is referred to as a “Multi VLAN Firewall”. Please refer to [Getting Started with FSA 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) for more details on getting started with this service. 
 
The previous options are a few possibilities you can explore if PPTP is required for your business needs, after the service is no longer provided by {{site.data.keyword.BluSoftlayer_notm}}. We thank you for your business.
{:note}

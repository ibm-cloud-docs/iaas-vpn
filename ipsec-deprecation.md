---

copyright:
  years: 2024
lastupdated: "2024-10-03"

keywords: deprecation, ipsec

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Deprecation of IPsec VPN
{: #ipsec-deprecation}

IPsec VPN is deprecated. As of 3 November 2024, you can't create new instances of IPsec VPN. Existing IPsec VPN instances are supported until 27 June 2025. Any instances that still exist on that date will be deleted.
{: deprecated}

## Important dates
{: #deprecation-timeline}

The following table describes the details of the deprecation, timeline, and extra information.

| Stage | Date | Description |
| --- | --- | --- |
| Deprecation announcement | 3 October 2024 | Announcement of the IPsec VPN deprecation. | Announcement of IPsec VPN deprecation. Existing instances will continue to run. |
| End of marketing | 3 November 2024 | No new instances of IPsec VPN can be created or purchased. Existing instances will continue to run. |
| End of support | 27 June 2025 | Running instances of IPsec VPN are permanently disabled and deprovisioned.|
{: caption="Table 1. Deprecation timeline" caption-side="bottom"}

## Deprecation details
{: #deprecation-details}

Review the following details about the IPsec VPN deprecation:

* After EOM (3 Nov 2024), you won't be able to create new IPsec VPN instances from the [IBM Cloud portal](/catalog/infrastructure/ipsec-vpn).
* After EOM (3 Nov 2024) and before EOS (27 Jun 2025), IPsec VPN will still be available to you for viewing and managing [your existing IPsec VPN instances](/classic/network/ipsecvpn).
* After EOS (27 Jun 2025), IPsec VPN is no longer supported for any orders, updates, or deletion operations. Any IPsec VPN tunnels and configurations will be cancelled and all existing IPsec VPN instances will be deleted and then reclaimed.

## Next steps for current users
{: #deprecation-next-steps}

In preparation for this transition, it is recommended that you migrate from IPsec VPN to IBM Cloud VPN for VPC or Gateway Appliances on classic.

### Before you begin
{: #before-you-begin-deprecation}

Plan your maintenance windows with your customer. With either of the migration options, the migration process will cause connection disruption.

### Option 1: Migrating to VPN for VPC
{: #migrate-vpnvpc}

VPN for VPC is an IPsec VPN solution on IBM Cloud Virtual Private Cloud (VPC) that securely extends your private network to IBM Cloud. VPN for VPC has the following advantages compared to IPsec VPN:

* More recent encryption and authentication algorithms
* Access to both VPC and Classic resources through integration with Transit Gateway
* High availability deployment
* Pay-as-You-Go pricing without any upfront monthly fee

#### Prerequsites: Enabling VRF for your account and creating a VPC
{: #migrate-vpnvpc-preq}

Your account must be enabled for Virtual Router Forwarding (VRF) if you choose to migrate to VPC.

If your account is not VRF-enabled, enable VRF in the **Account settings** menu of the IBM Cloud console. Learn more about the conversion process in [Enabling VRF in the console](/docs/account?topic=account-vrf-service-endpoint&interface=ui#vrf).

See also [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint&interface=ui) for more information about VRF conversion.

The update to an VRF account cannot be reverted. 
{: note}

Create a Virtual Private Cloud (VPC). See [user documentation](/docs/vpc?topic=vpc-getting-started) for the detailed instructions.

#### Creating VPN for VPC
{: #migrate-vpnvpc-prov}

Policy-based VPN mode is recommended for integration with Transit Gateway and access to classic.
{: important}

1. Read the [Planning considerations](/docs/vpc?topic=vpc-planning-considerations-vpn) before you start to create VPN for VPC.
1. Create a VPN gateway in policy-based mode. See VPN for VPC [user documentation](/vpc?topic=vpc-vpn-create-gateway&interface=ui) for more details.
1. Create a VPN connection between the VPN Gateway and your remote peer Gateway. See [user documentation](/docs/vpc?topic=vpc-vpn-adding-connections&interface=ui ) for more details.
1. Create a Transit Gateway in the same region. See Transit Gateway [user documentation](/docs/transit-gateway?topic=transit-gateway-getting-started) for more details.

   * Select **Local** routing.
   * Create two connections with your Transit Gateway instance: one to your VPC and the other to Classic environment. 
1. Create an ingress routing table and configure route propagation for VPN gateways. For more information, see [Configuring route propagation for VPN gateways](/docs/vpc?topic=vpc-advertise-routes-s2s).

   * Set **Accept routes from** to VPN gateway.
   * Set the traffic source as Transit Gateway and turn the **Advertise to** switch to *On*.
1. Set up the on-premises VPN gateway. Set both the VPC subnet and the classic subnet as remote CIDRs.

You should be able to access your classic Virtual Server Instance (VSI) from on-premises.

### Option 2: Migrating to gateway appliances
{: #migrate-gateway}

Alternatively you can choose to migrate to [Gateway Appliances](/catalog/infrastructure/gateway-appliance) on classic. Gateway Appliances are a series of router, firewall, and security appliances to protect your cloud infrastructure and optimize the performance.

Migrating to gateway appliances has the following benefits:

* High Availability (HA) deployement or non-HA deployment at your choice
* Central management
* Advanced security and VPN features besides IPsec VPN

Dependent on the gateway appliance type that you choose, read more about creating a gateway appliance in the user documentation:

* [Juniper vSRX](/docs/vsrx?topic=vsrx-getting-started)
* [Fortinet vFSA](/docs/vfsa?topic=vfsa-getting-started)

### Deleting IPsec VPN instances
{: #service-delete}

If you have converted your account to VRF, IPSec VPN stops working immediately. Only existing IPsec VPN instances within non-VRF accounts can continue to be used until End of Service (27 June 2025).
{: note}

After you successfully migrate to VPN for VPC or gateway appliances, delete your IPsec VPN instances using the following steps when you're ready.

1. Log in to the {{site.data.keyword.cloud}} console.
2. Navigate to the existing IPsec VPN [instance list](/classic/network/ipsecvpn).
3. In the Actions column, select **Delete**.

If you don't manually delete your IPsec VPN instances before End of Service (27 June 2025), they will be deleted and reclaimed on this date.

---

copyright:
  years: 1994, 2020
lastupdated: "2020-07-13"

keywords: VPN access, IBM Cloud VPN, user account

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

# Getting started with {{site.data.keyword.cloud_notm}} Virtual Private Networking
{: #getting-started}

Virtual Private Networking (VPN) access enables users to manage all servers remotely and securely over the {{site.data.keyword.cloud}} private network. A VPN connection from your location to the private network allows out-of-band management and server rescue through an encrypted VPN tunnel. VPN tunnels can be initiated to any IBM Cloud data center or PoP allowing you geographic redundancy.
{:shortdesc}

With VPN access, you can:

* Establish a VPN connection to the private network via SSL, or IPsec.
* Access your server through its primary private IP address by SSH or RDP.
* Connect to your server’s IPMI IP address for low-level server management or rescue needs.

A number of services require access through the private network, and VPN is one method that allows private network access. A VPN is good to use when you need to log in to the private network, do your work, and then log out. For example, this access often is needed to reach the KVM of the server.

Each user on an account can be given VPN access and can be limited regarding the subnets to which it needs access. The account user must have VPN access enabled and have a VPN password specified before attempting to login to VPN services.

## Enabling SSL VPN access
{: #enable-user-vpn-access}

To get started, you'll need to enable VPN access on each account that needs VPN access. To enable SSL VPN access, follow these steps:

1. Log in to the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){:external}.
1. Click **Manage > Access (IAM)**, and select **Users**.

   If you need to add a user, click **Add VPN-only user** or **Invite users**. For more information, see [Inviting users to an account](/docs/iam?topic=iam-iamuserinv){:external}.
   {:note}
1. Select the name of the user that you want to assign SSL VPN access.
1. From the Manage _User_ page, select the **Classic Infrastructure** tab and then click **VPN subnets**.
1. Select the **Enable SSL VPN Access** checkbox and click **Save**.

  For example:

  ![Enable SSL VPN Access](images/vpn_ssl_enable.png)

## Setting the VPN password
{: #set-vpn-password}

Your next step is to update the classic infrastructure VPN password. You can update your own VPN password, or in the case where a user forgets their password, another user with correct access can update that user's VPN password.

If you have the following access, you can update the VPN password for another user:

  * An IAM policy with the Editor or higher role on the User management service.
  * You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned.

To update the VPN password:

1. From the {{site.data.keyword.cloud_notm}} menu bar, click **Manage > Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the User details view, go to the **VPN password** section.

  ![Edit VPN password](images/vpn_password.png)

4. Click the **Edit** icon ![Edit icon](images/icon_write.svg) to enter a new VPN password.  
5. Click **Apply** to save your changes.

## Logging in to the VPN
{: #login-to-the-vpn}

Now that the VPN access is configured, you can log in by either using your browser or a standalone VPN client.

### Using a browser

1. Using Internet Explorer, click on any one of the [Available VPN endpoints](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints).
2. Follow the prompts to accept use of the SSL VPN client software.
3. When prompted, enter your VPN login credentials.

### Using a standalone SSL VPN client

See [Standalone VPN clients](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients) for available options and usage instructions.

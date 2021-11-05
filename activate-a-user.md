---

copyright:
  years: 1994, 2020
lastupdated: "2020-02-28"

keywords: SSL VPN access, user SSL VPN, IBM Cloud SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:DomainName: data-hd-keyref="DomainName"}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Activating or deactivating SSL VPN access for a user
{: #activate-or-deacivate-ssl-vpn-access-for-a-user}
{: help}
{: support}

To get started, you must enable VPN access on each account that needs VPN access. To enable SSL VPN access, follow these steps:

1. Log in to the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: external}.
1. Click **Manage > Access (IAM)**, and select **Users**.
   If you need to add a user, click **Add VPN-only user** or **Invite users**. For more information, see [Inviting users to an account](/docs/account?topic=account-iamuserinv){: external}.
   {: note}
   
1. Select the name of the user that you want to assign SSL VPN access.
1. From the Manage _User_ page, select the **Classic Infrastructure** tab and then click **VPN subnets**.
1. Select the **Enable SSL VPN Access** checkbox and click **Save**.

   For example:

   ![Enable SSL VPN Access](images/vpn_ssl_enable.png){: caption="Enable SSL VPN Access" caption-side="bottom"}  

   SSL access must be activated before a user can connect by using SSL.
   {: note}

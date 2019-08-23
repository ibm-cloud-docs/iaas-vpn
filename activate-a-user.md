---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-08-21"

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

# Activate or deactivate SSL VPN access for a user
{:#activate-or-deacivate-ssl-vpn-access-for-a-user}

SSL VPN enables a user to create a secure tunnel from a remote desktop to the {{site.data.keyword.cloud_notm}} private network, using a standard web browser. The {{site.data.keyword.cloud_notm}} SSL VPN is compatible with Java-capable web browsers, and the SSL VPN service is provided free to all users. Activate or deactivate SSL VPN access for a user with these steps:

1. Navigate to the {{site.data.keyword.cloud_notm}} [dashboard](https://{DomainName}/).
1. From the **Classic Infrastructure** section, select **User list**.
1. In the **Users** page, scroll to the user's name, or use the **Filter** option to search the list.
1. Select the **List of actions** menu icon in the user's entry, and choose **Manage user details**. 
1. In the **Manage** page, select the Classic Infrastructure tab.
1. From the **Permissions** tab, expand the **Network** menu. 
1. Select or deselect **Manage IPSEC Network Tunnels** to activate or deactivate SSL VPN access for that user.

**Note:** SSL access must be activated before a user can connect using SSL.

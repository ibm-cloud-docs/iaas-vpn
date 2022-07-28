---

copyright:
  years: 1994, 2022
lastupdated: "2022-07-27"

keywords: subnet access, IBM Cloud, VPN access

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Customizing SSL VPN subnet access
{: #customize-subnet-access}
{: help}
{: support}

{{site.data.keyword.BluSoftlayer_notm}} allows customers to set up VPN access from user accounts to specific private subnets. This setup must be performed by a user with VPN administration access, such as a local system administrator.
{: shortdesc}

To customize subnet access, navigate to the VPN interface and follow these steps:

1. Select the **Manual** radio button in the **Subnets** column.
1. Select the **Edit** link in the **Manual Overrides** column.
1. Select or clear the checkboxes in the **Grant Access** column of the subnets for which you want to update accessibility.
1. Select the **Save** link to apply your changes. Or, select the **Cancel** link to return to the previous screen without saving your changes.

If you have more than 64 subnets on an account, you will not be able to access your device/subnet. When you have your SSL VPN subnet assignment assigned to `Automatic`, it only provides you access with the first 64 subnets on the account; the other subnets aren't included. To fix this issue, you can set your SSL VPN subnet assignment to `Manual` and manually select the devices/subnets where your user need access.
{: note}

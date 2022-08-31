---

copyright:
  years: 2022
lastupdated: "2022-08-17"

keywords: 

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Why am I able to log in to the SSL VPN, but not able to access any devices?
{: #troubleshoot-no-access}
{: troubleshoot}
{: support}

SSL VPN is showing connected but no access is present to device.
{: shortdesc}

SSL VPN is showing connected but you cannot ping, rdp, ssh, KVM console or telenet to an internal device IP that belong to your IBM Cloud Infrastructure device.
{: tsSymptoms}

Possible causes include, but are not limited, to the following:

1. SSL VPN Subnet is incorrectly selected.
1. User doesn't have proper permissions to specific device or subnet.
1. More than 64 subnets exist on the account and user's SSL subnet is set to 'auto'.
1. User may be connected to another VPN causing some local routing issue.
1. Software was not ran by an "administrator" level user and routes were not implemented to the system's routing table.
1. Outbound connection are allowing the connection but other limitations may exist.
1. Old versions of SSL VPN software are known to cause routing problems on both Windows and Mac.
{: tsCauses}

1. Ensure that you are disconnected from all other VPNs before connecting to the SSL VPN.
1. Attempt to ping `10.0.80.11` while logged into the SSL VPN. If the ping is successful, this means that you have access to the internal network, but most likely do not have permission to access your devices.
1. Ensure that your user is given the correct and necessary permissions through the IBM Cloud console to access the device/subnet that you are attempting to access. To do this, an account admin must follow these steps:
   * Log in to your [{{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external} account.
   * Select **Manage** > **Access (IAM)**, then click **Users**.
   * Click the user name, then click the **Classic infrastructure** tab.
   * From the **Devices** and **VPN subnets** views, you can provide the user with VPN access to all the needed devices or subnets
   
      If you have more than 64 subnets on an account, you will not be able to access your device/subnet. When you have your SSL VPN subnet assignment assigned to `Automatic`, it only provides you access with the first 64 subnets on the account; the other subnets aren't included. To fix this issue, you can set your SSL VPN subnet assignment to `Manual` and manually select the devices/subnets where your user need access.
      {: note}

      To check the number of subnets on your account, go to the [Subnets](https://cloud.ibm.com/networking/subnets){: external} page, then locate the number before the word “Items” at the end of the page. This is the number of subnets that you have on the account.
      {: tip}
      
1. If you were not able to ping the DNS server, log out of the VPN and toggle your SSL VPN access from on to off, then off to on. For more information click [Activating or deactivating SSL VPN access for a user](/docs/iaas-vpn?topic=iaas-vpn-activate-or-deacivate-ssl-vpn-access-for-a-user).
1. If you have exhausted all the above steps and are still running into the issue, create an [IBM Support case](https://cloud.ibm.com/unifiedsupport/cases/form){: external}.
{: tsResolve}

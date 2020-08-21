---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-04-26"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Connecting to SSL VPN (Windows 7 and higher)
{:#connect-ssl-vpn-windows7}
{: help}
{: support}

To connect to the {{site.data.keyword.BluSoftlayer_notm}} SSL VPN, you must turn off User Access Control (UAC), enable the Administrator account, and ensure that you **Run as administrator** before you connect to the SSL VPN page.
{:shortdesc}

Follow these steps on your computer:

1. Turn off UAC:

  1. Select **Start > Control Panel > User Accounts > Change User Account Control Settings**.
  1. Clear the **Use User Account Control (UAC) to help protect your computer** checkbox, or drag the slider down to **Never notify**. Then, click **OK**.

1. Enable the Administrator account:

  1. Select **Start > Control Panel > Administrative Tools > Computer Management > Local Users and Groups > Users**.
  1. Right-click the **Administrator** user and select **Properties**.
  1. Clear the **Account is disabled** checkbox and click **OK**.

1. Ensure that your browser is set to **Run as administrator** before you connect to the SSL VPN page.

After you complete these steps, you can log in.

## Logging in
{:#connect-ssl-windows-login}

1. Ensure that your user has [VPN access](/docs/iaas-vpn?topic=iaas-vpn-activate-or-deacivate-ssl-vpn-access-for-a-user).
2. Review the list of [Available VPN endpoints](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints), and select a location near you.
3. Follow the prompts to accept use of the VPN client software.
4. When prompted, enter your VPN login credentials.

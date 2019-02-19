---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-18"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connect to SSL VPN - Windows 7 and higher

To connect to the {{site.data.keyword.BluSoftlayer_notm}} SSL VPN, you may need to do a few steps on your computer to ensure your ability to connect.

**1. Turn off User Access Control (UAC) in the control panel**

1. Navigate to **Start -> Control Panel -> User Accounts -> Change User Account Control Settings**
* **Uncheck** the box next to **Use User Account Control (UAC) to help protect your computer**.

**2. Enable the Administrator Account**

1. Go to **Start -> Control Panel -> Administrative Tools -> Computer Management -> Local Users and Groups -> Users ->** 
* Right-click the **Administrator** user and select **Properties** 
* Uncheck the box for **Account is disabled**.

**3. Run Internet Explorer as Administrator before connecting to the SSL VPN page**

1. Right-click on the Internet Explorer icon and select **Run as administrator** from the menu.

Once the previous steps are complete, you should be able to log in. 

## Log In

1. Go to [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) and log in using your portal username and password. 
* Be sure your user [has SSL VPN Access](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user).  
* Also, be sure that you have set a VPN password. To do so, update your [User Profile Page](https://control.softlayer.com/account/user/profile) and fill out the box that says **VPN Password**.

---

copyright:
  years: 1994, 2021
lastupdated: "2021-11-01"

keywords: standalone VPN clients, Virtual Private Network, MotionPro

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Connecting to SSL VPN from MotionPro clients (Windows, Linux, and Mac OS X)
{: #standalone-vpn-clients}

## Prerequisite
{: #standalone-prereqs}

* If you have never installed MotionPro clients, [log in to SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started#login-to-the-vpn) using the web browser. The compatible version of MotionPro client is available for you to download and install.
* If you have already installed the compatible version of MotionPro client, launch it directly from local.  
* In rare occasions (for example, incompatible browsers), you might want to download MotionPro clients manually from the [Array Networks Clients and Tools page](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html){: external}.

## Windows stand-alone client
{: #windows-standalone-client}

To install and set up MotionPro on Windows, follow these steps:

1. Run the MotionPro Setup Wizard. Then, click the MotionPro icon on your desktop and select **Profile > Add**.
1. To create a profile, enter a Site Name (domain name or IP address) and Host (select from available [VPN endpoints](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints)). Next, enter your VPN username and password and click **Save**.
1. Double-click the profile that you created to connect to the VPN.

If you have issues, uninstall any Array programs by using the Windows Control Panel, restart, and then reconnect.

   MotionPro does not work on Windows 8 RT.
   {: note}

## Linux stand-alone client
{: #linux-standalone-client}

To install and set up MotionPro on Linux, follow these steps:

1. Make it executable. For example: `chmod +x MotionPro_Linux_Ubuntu_x86-64_1.2.3.sh`
1. Run the script to install. For example: `./MotionPro_Linux_Ubuntu_x86-64_1.2.3.sh`

   * Usage:  `./MotionPro --host [site] --user [username] --passwd [password]`
   * To stop it:  `[control-c]`

1. Enable `rc.local`, if needed. For example:

   ```sh
     # If you are using systemd, you might not have the /etc/rc.local file, and you will get an "Auto start script file was not found in system!" error.
     # Make an empty one. systemd will know what to do with it
     # <https://askubuntu\.com/a/919598>

     $ printf '%s\n' '#!/bin/bash' 'exit 0' | sudo tee -a /etc/rc.local
     $ sudo chmod +x /etc/rc.local

     # Try installing again
     $ sudo ./MotionPro_Linux_Ubuntu_x86-64_1.2.3.sh
   ```      

To start the MotionPro client, you must input at least the `hostname` and `username` as arguments. `Site` can be either a domain name or an IP address.
{: tip}

## MotionPro StandAlone Mac OS X
{: #motionpro-standalone-client-mac}

To install and set up MotionPro on Mac OS, follow these steps for your particular version.

Uninstall any previous versions of the client before you install a new version.
{: important}

1. Open the MotionPro Plus application.
1. Click **Profile**, then **Create**. The Create Profile window shows.
1. Enter the following information:
   * Profile Name
   * Virtual Site Host
   * Virtual Site Port
   * User Name
   * Password

   ![Create Profile window](images/mac-standalone.png){: caption="Create Profile window" caption-side="bottom"}

1. Select the newly created profile, then click **Connect**.

   ![Connecting to virtual site host](images/mac-standalone-connect.png){: caption="Connecting to virtual site host" caption-side="bottom"}

   Status shows **Connecting**.

If the tunnel isn't directing traffic correctly, you might need to [add routes manually](https://discussions.apple.com/thread/2735376){: external}.
{: note}

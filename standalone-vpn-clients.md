---

copyright:
  years: 1994, 2024
lastupdated: "2024-01-02"

keywords: standalone VPN clients, Virtual Private Network, MotionPro

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Connecting to SSL VPN from MotionPro clients (Windows, Linux, and Mac OS X)
{: #standalone-vpn-clients}

## Prerequisites
{: #standalone-prereqs}

* If you have never installed MotionPro clients, [log in to SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started#login-to-the-vpn) using the web browser. The compatible version of MotionPro client is available for you to download and install.
* If you already installed a compatible version of the MotionPro client, launch it directly from local.  
* On rare occasions, such as if you have an incompatible browser, you might want to download MotionPro clients manually from the [Array Networks Clients and Tools page](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html){: external}. 

Uninstall any previous versions of the client and restart your system before you install a new version.
{: important}

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

* To install and set up MotionPro on Linux, follow these steps:
   
   1. Download: `wget --no-check-certificate [latest MotionPro link]`
   1. Make the file executable. For example: `chmod +x MotionPro_Linux_Ubuntu_x64_build-9.sh`
   1. Run as a superuser. For example: `sudo ./MotionPro_Linux_Ubuntu_x64_build-9.sh`
   
* To launch the GUI:

`$ MotionPro` -- This launches the GUI for the VPN client. Proceed to set up the VPN profile.

* To launch MotionPro using a command line:

`cd /opt/MotionPro`
`sudo ./vpn_cmdline -h [hostname] -u [username] -p [password]` -- The 'hostname' argument is the SSL VPN endpoint. For example: 'vpn.dal.softlayer.com'

* To stop MotionPro:

`sudo ./vpn_cmdline -s`

The preceding steps do not work with Linux installed on Windows. MotionPro will authenticate, but will not establish a connection.
{: note}

## MotionPro stand-alone clients for Mac OS X
{: #motionpro-standalone-client-mac}

### If you start from the Web browser and use the automatically downloaded MotionPro client
{: #web-browser-auto-install-motionpro}

If you have ever [logged on to SSL VPN](/docs/iaas-vpn?topic=iaas-vpn-getting-started#login-to-the-vpn) using a Web browser, the compatible version of MotionPro client is downloaded for you to install.

1. Next time you click on the wanted VPN endpoint from the [VPN endpoint page](https://www.ibm.com/cloud/vpn-access) and log in, the client is automatically launched. 
1. A profile for the selected endpoint is automatically loaded in your Web-launched MotionPro client. You do not have to create a new profile.
1. Click **Connect**.

The automatically downloaded MotionPro client does not work on MacOS Monterey (Version 12.x).
{: note}

### If you are using the manually installed MotionPro clients
{: #manually-installed-motionpro-clients}

If you have downloaded and installed the MotionPro client manually from the following pages, complete these steps to configure a connection.

* Mac OS MotionPro client on the [Array Networks Clients and Tools page](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html){: external}
* Mac OS MotionPro client (Web-Launched MP Client) on the [Array Networks Clients and Tools](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html){: external} website.

The MotionPro Plus clients, located in the [Apple Store](https://apps.apple.com/us/app/motionpro-plus/id1218085720?mt=12){: external}, are not supported. 
{: important}

1. Open the Mac MotionPro or MotionPro Plus application.
1. Click **Profile**, then **Create**. The Create Profile window shows.
1. Enter the following information:

   * Profile Name
   * Virtual Site Host
   * Virtual Site Port
   * User Name
   * Password
   
1. Select the newly created profile, then click **Connect**. Status shows **Connecting**. 
 
   If the tunnel isn't directing traffic correctly, you might need to [add routes manually](https://discussions.apple.com/thread/2735376){: external}.
   {: note}

If you run into issues installing the MotionPro or MotionPro Plus client, refer to the [Troubleshooting](/docs/iaas-vpn?topic=iaas-vpn-motionpro-pkg-error) section for assistance.
{: important}

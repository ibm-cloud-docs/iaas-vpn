---

copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-05-02"

keywords: Standalone VPN clients, Virtual Private Network, MotionPro

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:deprecated: .deprecated}
{:pre: .pre}
{:codeblock: .codeblock}

# Standalone VPN clients - Windows, Linux, and Mac OS X
{: #standalone-vpn-clients}

## Windows standalone client
{: #windows-standalone-client}

1. Download one of these files, depending on your operating system.
  * Windows (8/7/Vista/XP) 32-bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip
  * Windows (8/7/Vista/XP) 64-bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

2. Install and set up.
  * Run MotionProSetup to install the software.
  * Run MotionPro, then at the opening screen select **Profile > Add**.
  * Create a profile by giving it a Site Name, then choose a hostname from the list of [SSL VPN sites](#ssl-vpn-pops). Next, enter your VPN username and password and press **Save**.
  * Finally, double-click the profile you just created to connect to the VPN.

`Site` may be either a domain name or an IP address. 

If you have issues, uninstall any Array programs using the Windows Control Panel, reboot, then reconnect.

Does not work on Windows 8 RT.
{:note}

## Linux standalone client
{: #linux-standalone-client}

1. Download the appropriate MotionPro client for your Linux distribution. For this example, we use Ubuntu.
  * CentOS 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.1.1.sh
  * Redhat 32-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.1.1.sh
  * Redhat 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.1.1.sh
  * Ubuntu 32-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.1.1.sh
  * Ubuntu 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.1.1.sh

2. Make it executable: `chmod +x MotionPro_Linux_Ubuntu_x86-64_1.1.1.sh`

3. Run the script:  `./MotionPro_Linux_Ubuntu_x86-64_1.1.1.sh.`
  * Usage:  `./MotionPro --host [site] --user [username] --passwd [password]`
  * To stop it:  `[control-c]`

4. Enable rc.local, if needed.
    
  ```
     # If you are using systemd, you might not have /etc/rc.local file, and you will get an error that says "Auto start script file was not found in system!"
     # Make an empty one. systemd will know what to do with it
     # <https://askubuntu\.com/a/919598>

     $ printf '%s\n' '#!/bin/bash' 'exit 0' | sudo tee -a /etc/rc.local
     $ sudo chmod +x /etc/rc.local

     # Try installing again
     $ sudo ./MotionPro_Linux_Ubuntu_x86-64_1.1.1.sh
```     

To start the MotionPro client, you must input at least the `hostname` and `username` as arguments. `Site` may be either a domain name or an IP address.
{:tip}

## Mac OS X 10.10 standalone client
{: #macos-standalone-client}

MacOS 10.11 is not supported. 
{:note}

Steps for the MacOS StandAlone Array SSL VPN Motion Pro Plus client:

1. Install the "Motion Pro Plus" client from the Apple store.
  * Locate the  Motion Pro Plus client under the **Applications** folder and open the application.
  * Click **Profile**, then **Add**.
  * Fill in the Site Name, Host, and Username information, then click **Ok**.
  * Click **VPN** at the top left, then **Connect**.

An example is detailed below:

![Figure 1](images/snip20170425_1.png)

If the tunnel isn't directing traffic correctly, you may need to [add routes manually](https://discussions.apple.com/thread/2735376).

Uninstall any previous versions before updating.
{:important}

## Array Networks VPN Standalone Client
{: #array-networks-vpn-standalone-client}

If any of the clients mentioned earlier in this document do not work for you, check the Array Networks [Clients and Tools](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html) support page for a list of downloadable links to Windows, Linux, and MacOS standalone clients.

## SSL VPN POPs (sites)
{: #ssl-vpn-pops}

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


Uninstall any previous versions of the client before installing the new version.
{:important}

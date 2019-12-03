---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-11-11"

keywords: IPSec VPN, IP address, IP traffic, IaaS VPN, Fedora, Windows, Linux, SSL VPN

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

# Setting up an SSL VPN connection
{:#setup-ssl-vpn-connections}

Windows, Linux Fedora, and Linux require individualized connection instructions.
{:shortdesc}

Here are some examples of how you can use an SSL VPN connection:

* Remote desktop to your server's backend IP address (10.4.X.X) for administration of your Windows 2003 servers.
* SSH to your server's backend IP address (10.4.X.X) for administering your UNIX servers.
* Use an IPMI client to control your server using the backend IPMI address (10.4.X.X). You can download the IPMI client tool after you are connected by going to http://downloads.softlayer.local/ipmi/ (You must be connected to SoftLayer Private VPN.)
  **Note:** IPMIView requires Java to be installed.  http://www.sun.com/java/
* Testing your website on the backend IPs before you make them live on your public IPs.
* File transfer of secure data between your server(s) and your home/office.
* Backup of configuration files your server(s) to your home/office.
* Securely connect to our [{{site.data.keyword.cloud}} console](http://{DomainName}/){:external}.

## Windows  
{:#setup-ssl-vpn-connections-windows}

1. Open Internet Explorer and navigate to `https://www.ibm.com/cloud-computing/bluemix/vpn-access`.
* After you enter your username and password, you might be prompted to install an ActiveX plug-in. You must install this plug-in to connect to your backend network.
* You also must have administrative rights on your workstation to install the ActiveX plug-in. If you do not have rights to install the plug-in, ask your local system administrator to install it for you.
* After the ActiveX plug-in is installed, an Array SSL VPN network connector launches and establishes a connection to the VPN device. If successful, a red '**A**' appears in your taskbar. You can click the '**A**' at any time to see the status of your SSL VPN connection: its status, assigned IP address, assigned DNS servers, network routes, and time connected.
* You can minimize your browser session at any time and continue to use other applications securely on the private network.
* When you are finished, select the disconnect button to the right, or simply close the window.

## Linux Fedora
{:#setup-ssl-vpn-connections-linux}

Firefox no longer supports NPAPI plug-ins (java applets). Use a different browser to perform these steps.
{:note}

It is recommended that you run all commands as root. (`setuid root`)

1. Download Java from `http://java.com/en/download/manual.jsp`. This is a Linux self-extracting file.
* Close your browser.
* Move the file to where you want to install Java (usually in `/usr/local`)
* Make the file executable using the command `chmod +x jre-6u1-linux-i586.bin`
* Run the installer by using the command `./jre-6u1-linux-i586.bin`
* Agree to the terms and install.
* After installation completes, you must create a symlink.

## Linux example
{:#setup-ssl-vpn-connections-linux-example}

1. Open your browser and go to `https://www.ibm.com/cloud-computing/bluemix/vpn-access`.
* Log in with your console username and password.
* After you are connected, select the **Network** tab.
* A connect/install button appears. Select it and you should be prompted to install a Java component.
* Install the component in the default path, which you might have to create manually. (`/usr/local/array_vpn`)
* After it is installed, a window appears that states you are connected.
* This window must remain open to use the VPN tunnel, but you can minimize it.
* To test the connection, ping 10.0.80.11 or your server's private address. If you get a reply, you are connected successfully.
* When you are finished, select the disconnect button under the 'Network' tab, or close your browser windows.

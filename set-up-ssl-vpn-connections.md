---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-02"

keywords: IPsec VPN, IP address, IP traffic, IaaS VPN, Fedora, Windows, Linux, SSL VPN

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
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Setting up an SSL VPN connection
{:#setup-ssl-vpn-connections}
{: help}
{: support}

Windows, Linux, and macOS require individualized connection instructions.
{:shortdesc}

Here are some examples of how you can use an SSL VPN connection:

* Remote desktop to your server's backend IP address (10.X.X.X) for administration of your Windows 2012/2016 servers.
* SSH to your server's backend IP address (10.X.X.X) for administering your Linux servers.
* Use an IPMI client to control your server using the backend IPMI address (10.X.X.X). You can download the IPMI client tool after you are connected by going to [http://downloads.service.softlayer.com/ipmi/](http://downloads.service.softlayer.com/ipmi/). (You must be connected to SoftLayer Private VPN to access.)

   IPMIView requires Java to be installed.  
   {:note}
* Testing your website on the backend IPs before you make them live on your public IPs.
* File transfer of secure data between your servers and your home or office.
* Backup of configuration files your servers to your home or office.
* Securely connect to the [{{site.data.keyword.cloud}} console](https://cloud.ibm.com){:external}.

## Windows  
{:#setup-ssl-vpn-connections-windows}

1. Open Internet Explorer and select an [Available VPN endpoint](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints) to open a VPN web portal.
1. After you enter your username and password, you might be prompted to install an ActiveX plug-in.

   You must install this plug-in to connect to your backend network.

   You also must have administrative permissions on your workstation to install the ActiveX plug-in. If you do not have permission to install the plug-in, ask your local system administrator to install it for you.
1. After the ActiveX plug-in is installed, an Array SSL VPN network connector launches and establishes a connection to the VPN device. If successful, a red '**A**' appears in your taskbar. You can click the '**A**' at any time to see the status of your SSL VPN connection: its status, assigned IP address, assigned DNS servers, network routes, and time connected.
1. You can minimize your browser session at any time and continue to use other applications securely on the private network.
1. When you are finished, select the disconnect button to the right, or simply close the window.

## Linux Fedora
{:#setup-ssl-vpn-connections-linux}

Firefox no longer supports NPAPI plug-ins (Java applets). Use a different browser to perform these steps.
{:note}

It is recommended that you run all commands as root. (`setuid root`)

1. Download Java from `http://java.com/en/download/manual.jsp`. This is a Linux self-extracting file.
1. Close your browser.
1. Move the file to where you want to install Java (usually in `/usr/local`)
1. Make the file executable by using this command:

   `chmod +x jre-8u241-linux-i586.bin`
1. Run the installer by using the command:

   `./jre-8u241-linux-i586.bin`
1. Agree to the terms and install.
1. After installation completes, you must create a symlink.

## Linux example
{:#setup-ssl-vpn-connections-linux-example}

1. Go to [Available VPN endpoints](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints).
2. Select a VPN web portal link and log in with your console username and password.
3. After you are connected, select the **Network** tab.
4. A connect/install button appears. Select it and you are prompted to install a Java component.
5. Install the component in the default path, which you might have to create manually. (`/usr/local/array_vpn`)

   After it is installed, a window appears that states you are connected.

   This window must remain open to use the VPN tunnel, but you can minimize it.
8. To test the connection, ping `10.0.80.11` or your server's private address. If you get a reply, you are connected successfully.
9. When you are finished, select the disconnect button under the 'Network' tab, or close your browser windows.

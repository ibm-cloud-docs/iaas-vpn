---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Set up PPTP VPN for Windows 7

PPTP VPN connection allows remote connection to the {{site.data.keyword.BluSoftlayer_notm}} Private Network from a desktop or dedicated device. Connecting to the Private Network through PPTP is available for multiple operating systems, including Windows 7. Users may connect to any {{site.data.keyword.BluSoftlayer_notm}} data center by entering the data center's unique destination address during setup. Follow the steps below to set up a PPTP VPN connection in Windows 7.

## Set up a PPTP VPN Connection

1. Refer to Microsoft's [How-To Page](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} to reach the screen to set up the remote connection.

2. Enter the destination address of the desired data center in the internet address field. Refer to the table below for the appropriate addresses for current IBM Cloud data centers.

|Data Center Location|Data Center Internet Address|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapore, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, HK|pptpvpn.hkg02.softlayer.com|
|Melbourne, AU|pptpvpn.mel01.softlayer.com|
|London, GB|pptpvpn.lon02.softlayer.com|
|Paris, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokyo, JP|pptpvpn.tok02.softlayer.com|

3\. Enter an identifying name for the connection in the **Destination name** field.

**Note:** We recommend using the data center location as the Destination name.

4\. Enter your [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) Username in the **User Name** field.

5\. Enter your **VPN Password** in the **Password** field.

6\. Click the **Connect** button.

7\. Now, on you're computer, you'll need to disable the remote gateway so you can connect to the internet as well as the VPN.

8\. Click **Start**, then open the **Control Panel** -> **Network and Sharing** -> **Change Adapter Settings**.

9\. Right-click on the PPTP VPN connection and click on **Properties**.

10\. Uncheck the TCP/IPv6 box, and then click on the TCP/IPv4 and click properties.

11\. Click the **Advanced** button.

12\. Uncheck the box for **Use Default Gateway on Remote Network** and then select **OK**.

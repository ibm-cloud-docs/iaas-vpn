---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Set Up PPTP VPN for Mac OS X 10.X

PPTP VPN connection allows remote connection to the {{site.data.keyword.BluSoftlayer_notm}} Private Network from a desktop or dedicated device. Connecting to the Private Network through PPTP is available for multiple operating systems, including Mac OS X. Users may connect to any {{site.data.keyword.BluSoftlayer_notm}} data center by entering the data center's unique destination address upon setup.  Follow the steps below to set up a PPTP VPN connection in Mac OS X.

## Set Up a PPTP VPN Connection

* Select **System Preferences** from the **Apple Menu** drop down.
* Click the **Network** icon in the Internet&Network section.
* Click the **Plus Sign** icon at the bottom on the **Connections** menu.  A pop-up box appears to let you create the VPN Connection.
* Create the VPN Connection.
  * Select **VPN** from the **Interface** drop down list.
  * Select **PPTP** from the **VPN Type** drop down list.
  * Enter a **descriptive title** for the connection in the **Service Name** field.
  * **Note:** We recommend using the Data Center location as part of the Service Name.
  * Click the **Create** button.
* Click on the connection that was just created in the Connections menu.
* Enter the **destination address** of the desired data center in the **Server Address** field.  Refer to the table below for the appropriate addresses for current {{site.data.keyword.BluSoftlayer_notm}} data centers.
* Enter your **Customer Portal User Name** in the **Account name** field.
* Complete the Authentication Settings.
  * Click the **Authentication Settings** button.  A pop-up box will appear prompting authentication of the VPN.
  * Enter your **Customer VPN Password** in the **Password** field.
  * Click the **OK** button.
* Update the VPN Traffic settings.
  * Click the **Advanced** button.
  * Ensure that the **Send all traffic over VPN Connection** check box in the Session section is not selected.
  * Click the **OK** button.
* Select the **Show VPN Status in menu bar** check box.
* Click the Apply button.  The VPN connection may now be established at any time using the VPN Menu bar item.

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

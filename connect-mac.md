---
copyright:
  years: 1994, 2018
lastupdated: "2018-10-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connect to SSL VPN – macOS

Install the latest version of the MotionPro client from the [Array Networks website](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html). Be sure to uninstall any previous versions before updating.

After you install the new client, go to the following directory and launch the VPN using the Terminal application. 

`/usr/local/motionpro/`

From there, run the following command to get connected to the SSL VPN:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

A list of VPN endpoints can be found [here](https://www.softlayer.com/vpn-access).

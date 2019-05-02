---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connect to SSL VPN – MAC OSX 10x and higher
{:#connect-ssl-vpn-mac-osx}

Install the latest version of Mac MotionPro client v1.1.7 from the Apple Store. Be sure to uninstall any previous versions before updating.

After you install the new client, go to the following directory and launch the VPN using the Terminal application. 

`/usr/local/motionpro/`

From there, run the following command to get connected to the SSL VPN:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

A list of VPN End-Points can be found [here](https://www.softlayer.com/vpn-access).
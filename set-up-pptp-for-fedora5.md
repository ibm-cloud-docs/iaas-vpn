---
copyright:
  years: 1994, 2017
lastupdated: "2018-05-18"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Set up PPTP for Fedora Core 5

You'll need to install and configure.

**1. Installation**
Install PPTP and the `pptpconfig` GUI using one of the following commands:
```
# rpm -Uvh http://pptpclient.sourceforge.net/yum/stable/fc5/pptp-release-current.no...
# yum --enablerepo=pptp-stable install pptpconfig
```

**2. Configuration**

1. IBM Cloud PPTP information:

|Field|Entry|
|-----|-----|
|Server:|<ul><li>pptpvpn.dal01.softlayer.com (Dallas)</li><li>pptpvpn.sea01.softlayer.com (Seattle)</li><li>pptpvpn.wdc01.softlayer.com (Washington D.C.)</li></ul>|
|Domain Name:|Leave blank|
|Username:|(example: SL12345)|
|Password:|  |


2. Run *pptpconfig* <span style="text-decoration: underline">as root</span>, and a window should appear,<br/>
![Figure 1](images/ss1.jpeg)

3. Enter the name, server, username and password into the Server tab.

4. In the Encryption section leave everything the default for it works for most customers.<br/>
![Figure 2](images/ss2.jpeg)

5. Click on *Add*, and the tunnel will appear in the list,

6. Click on the tunnel to select it, click on *Start*, and a window will appear with the tunnel connection log and status,

7. If the connection fails, you might need to gather more information, so on the *Miscellaneous* tab, click on *Enable connection debugging facilities*, click *Update*, try *Start* again, then look at the [Diagnosis HOWTO](http://pptpclient.sourceforge.net/howto-diagnosis.phtml){:new_window} for whatever error is displayed.<br/>
![Figure 3](images/ss3.jpeg)

8. If the connection succeeded, you can try the Ping test button. If the ping fails, you should try to find out why before proceeding. If the ping works, then the tunnel is active and you may now work on routing.

9. Only the IPs that live in the backend network at IBM Cloud should be routed across this VPN tunnel.  *Stop* the tunnel, select it again, then click on either *Client to LAN or LAN to LAN* on the *Routing* tab, use the *Edit Network Routes* button to enter '10.0.0.0/8' for the Network and 'SoftLayer' for the Name, and then try *Start* again. Now try to access your server's private IP address or SoftLayer's private name server at 10.0.80.11.<br/>
![Figure 4](images/ss4.jpeg)

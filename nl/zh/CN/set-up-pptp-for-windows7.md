---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 针对 Windows 7 设置 PPTP VPN

通过 PPTP VPN 连接，可从台式机或专用设备远程连接到 {{site.data.keyword.BluSoftlayer_notm}} 专用网络。通过 PPTP 连接到专用网络在多种操作系统（包括 Windows 7）中可用。用户可通过在设置期间输入数据中心的唯一目标地址来连接到任何 {{site.data.keyword.BluSoftlayer_notm}} 数据中心。请执行以下步骤在 Windows 7 中设置 PPTP VPN 连接。

## 设置 PPTP VPN 连接

1. 请参阅 Microsoft [操作指南页面](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window}，以访问用于设置远程连接的屏幕。

2. 在“因特网地址”字段中，输入所需的数据中心的目标地址。有关当前 IBM Cloud 数据中心的相应地址，请参阅下表。

|数据中心位置|数据中心因特网地址|
|---|---|
|得克萨斯州达拉斯|pptpvpn.dal01.softlayer.com|
|华盛顿州西雅图|pptpvpn.sea01.softlayer.com|
|加利福尼亚州圣何塞|pptpvpn.sjc01.softlayer.com|
|华盛顿特区|pptpvpn.wdc01.softlayer.com|
|荷兰阿姆斯特丹|pptpvpn.ams01.softlayer.com|
|新加坡新加坡市|pptpvpn.sng01.softlayer.com|
|得克萨斯州休斯敦|pptpvpn.hou02.softlayer.com|
|中国香港特别行政区|pptpvpn.hkg02.softlayer.com|
|澳大利亚墨尔本|pptpvpn.mel01.softlayer.com|
|英国伦敦|pptpvpn.lon02.softlayer.com|
|法国巴黎|pptpvpn.par01.softlayer.com|
|加拿大多伦多|pptpvpn.tor01.softlayer.com|
|日本东京|pptpvpn.tok02.softlayer.com|

3\. 在**目标名称**字段中，输入连接的标识名称。

**注：**建议使用数据中心位置作为“目标名称”。

4\. 在**用户名**字段中，输入[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 的用户名。

5\. 在**密码**字段中，输入 **VPN 密码**。

6\. 单击**连接**按钮。

7\. 现在，您需要在计算机上禁用远程网关，以便可连接到因特网和 VPN。

8\. 单击**开始**，然后打开**控制面板** -> **网络和共享** -> **更改适配器设置**。

9\. 右键单击 PPTP VPN 连接，然后单击**属性**。

10\. 取消选中 TCP/IPv6 框，然后单击 TCP/IPv4 并单击“属性”。

11\. 单击**高级**按钮。

12\. 取消选中**在远程网络上使用默认网关**复选框，然后选择**确定**。

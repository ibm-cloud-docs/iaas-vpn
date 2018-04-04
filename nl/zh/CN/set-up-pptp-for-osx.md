---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 针对 Mac OS X 10.X 设置 PPTP VPN

通过 PPTP VPN 连接，可从台式机或专用设备远程连接到 {{site.data.keyword.BluSoftlayer_notm}} 专用网络。通过 PPTP 连接到专用网络在多种操作系统（包括 Mac OS X）中可用。用户可通过在设置时输入数据中心的唯一目标地址来连接到任何 {{site.data.keyword.BluSoftlayer_notm}} 数据中心。请执行以下步骤在 Mac OS X 中设置 PPTP VPN 连接。

## 设置 PPTP VPN 连接

* 从 **Apple 菜单**下拉列表中，选择**系统偏好设置**。
* 在“互联网和网络”部分中，单击**网络**图标。
* 在**连接**菜单上，单击底部的**加号**图标。这将显示一个弹出框，允许您创建 VPN 连接。
* 创建 VPN 连接。
  * 从**接口**下拉列表中，选择 **VPN**。
  * 从 **VPN 类型**下拉列表中，选择 **PPTP**。
  * 在**服务名称**字段中，输入连接的**描述性标题**。
  * **注：**建议使用数据中心位置作为“服务名称”的一部分。
  * 单击**创建**按钮。
* 单击刚刚在“连接”菜单中创建的连接。
* 在**服务器地址**字段中，输入所需数据中心的**目标地址**。有关当前 {{site.data.keyword.BluSoftlayer_notm}} 数据中心的相应地址，请参阅下表。
* 在**帐户名称**字段中，输入**客户门户网站用户名**。
* 完成认证设置。
  * 单击**认证设置**按钮。这将显示一个弹出框，提示您对 VPN 进行认证。
  * 在**密码**字段中，输入**客户 VPN 密码**。
  * 单击**确定**按钮。 
* 更新“VPN 流量”设置。
  * 单击**高级**按钮。
  * 确保未选中“会话”部分中的**通过 VPN 连接发送所有流量**复选框。
  * 单击**确定**按钮。 
* 选中**在菜单栏中显示 VPN 状态**复选框。
* 单击“应用”按钮。现在可随时使用 VPN 菜单栏项来建立 VPN 连接。

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

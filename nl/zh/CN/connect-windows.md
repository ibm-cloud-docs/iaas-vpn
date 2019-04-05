---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 连接到 SSL VPN - Windows 7 和更高版本
{:#connect-ssl-vpn-windows7}

要连接到 {{site.data.keyword.BluSoftlayer_notm}} SSL VPN，您可能需要在计算机上执行一些步骤以确保您能够进行连接。

**1. 在控制面板中关闭用户访问控制 (UAC)**

1. 浏览至**开始 -> 控制面板 -> 用户帐户 -> 更改用户帐户控制设置**
* **取消选中****使用用户帐户控制 (UAC) 帮助保护您的计算机**旁边的框。

**2. 启用管理员帐户**

1. 转至**开始 -> 控制面板 -> 管理工具 -> 计算机管理 -> 本地用户和组 -> 用户 ->** 
* 右键单击 **Administrator** 用户，然后选择**属性** 
* 取消选中**帐户已禁用**对应的框。

**3. 在连接到 SSL VPN 页面之前，以管理员身份运行 Internet Explorer**

1. 右键单击 Internet Explorer 图标，然后从菜单中选择**以管理员身份运行**。

完成上述步骤后，您应该能够登录。 

## 登录
{:#connect-windows-login}

1. 转至 [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) 并使用您的门户网站用户名和密码登录。 
* 确保用户[具有 SSL VPN 访问权](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user)。  
* 另外，请确保已设置 VPN 密码。为此，请更新[用户概要文件页面](https://control.softlayer.com/account/user/profile)，填写显示 **VPN 密码**的框。

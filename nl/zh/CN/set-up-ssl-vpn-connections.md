---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Linux Fedora, SSL VPN connections Windows, backend IP address

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 设置 SSL VPN 连接
{:#setup-ssl-vpn-connections}

Windows、Linux Fedora 和 Linux 需要在本文档中所示的个性化连接指示信息。下面是如何使用 SSL VPN 连接的一些示例：

* 从远程桌面连接到服务器的后端 IP 地址 (10.4.X.X)，以管理 Windows 2003 服务器。
* 通过 SSH 连接到服务器的后端 IP 地址 (10.4.X.X)，以管理 UNIX 服务器。
* 使用 IPMI 客户机通过后端 IPMI 地址 (10.4.X.X) 来控制服务器。连接后，可以通过转至 http://downloads.softlayer.local/ipmi/（必须连接到 SoftLayer 专用 VPN）来下载 IPMI 客户机工具。
  * **注：**IPMIView 需要安装 Java (http://www.sun.com/java/)。
* 使 Web 站点在公共 IP 上运行之前，请先在后端 IP 上测试 Web 站点。
* 在服务器与家庭/办公室之间进行安全数据的文件传输。
* 将服务器的配置文件备份到家庭/办公室。
* 安全连接到我们的 [Web 门户网站](http://control.softlayer.com/)。

## Windows (Internet Explorer)
{:#setup-ssl-vpn-connections-windows}

1. 打开 Internet Explorer 并导航至 `http://www.softlayer.com/vpn-access`。
* 输入您的用户名和密码后，系统将提示您安装 ActiveX 插件。必须安装此插件才能连接到后端网络。 
* 您还必须具有工作站的管理权限才能安装 ActiveX 插件。如果您无权安装该插件，可请求本地系统管理员为您安装。 
* 安装 ActiveX 插件后，Array SSL VPN 网络连接器将启动并建立到 VPN 设备的连接。如果成功，任务栏中会显示一个红色的“**A**”。您可以随时单击“**A**”来查看 SSL VPN 连接的状态：其状态、分配的 IP 地址、分配的 DNS 服务器、网络路径和连接时间。 
* 您可以随时最小化浏览器会话以继续安全地使用专用网络上的其他应用程序。 
* 完成后，可以通过选择右侧的“断开连接”按钮来断开连接，也可以直接关闭窗口。

## Linux Fedora 
{:#setup-ssl-vpn-connections-linux}

Firefox 不再支持 NPAPI 插件 (java applet)。使用不同的浏览器执行这些步骤。
{:note}

建议以 root 用户身份运行所有命令。(`setuid root`)

1. 从 `http://java.com/en/download/manual.jsp` 下载 Java。这是 Linux 自解压文件。
* 关闭浏览器。
* 将该文件移至要安装 Java 的位置（通常位于 `/usr/local`）。
* 使用 `chmod +x jre-6u1-linux-i586.bin` 命令使该文件成为可执行文件。
* 使用 `./jre-6u1-linux-i586.bin` 命令运行安装程序。
* 同意相关条款并安装。
* 安装完成后，必须立即创建符号链接。

## Linux 示例
{:#setup-ssl-vpn-connections-linux-example}

1. 打开浏览器并转至 `http://www.softlayer.com/vpn-access`。
* 使用您的客户门户网站用户名和密码登录。
* 连接后，选择**网络**选项卡。
* 应该会看到“连接/安装”按钮。选择该按钮，系统应该会提示您安装 Java 组件。
* 将该组件安装在缺省路径中，您可能需要手动创建该路径 (`/usr/local/array_vpn`)。
* 安装后，应该会显示一个窗口，告知您已建立连接。
* 此窗口必须保持打开状态才可利用 VPN 隧道，但您可以将此窗口最小化。
* 要测试连接，请对 10.0.80.11 或服务器的专用地址执行 ping 操作。如果收到回复，说明已成功连接。
* 完成后，选择“网络”选项卡下的“断开连接”按钮，或者只需关闭所有浏览器窗口。

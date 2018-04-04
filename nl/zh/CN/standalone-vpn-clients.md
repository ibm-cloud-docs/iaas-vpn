---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 独立 VPN 客户机 - Windows、Linux 和 Mac OS X

## Windows 独立客户机

Windows (8/7/Vista/XP) 32 位：https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) 64 位：https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. 根据您的操作系统，下载上面列出的其中一个文件。
* 运行 MotionProSetup 以安装软件。
* 运行 MotionPro 并在打开的屏幕上，选择**概要文件 -> 添加**。
* 通过为概要文件提供“站点名称”，然后从 SSL VPN 站点列表（如下所示）中选择主机名来创建概要文件。接着输入您的 VPN 用户名和密码，然后按**保存**。
* 最后，双击刚才创建的概要文件以连接到 VPN。

**注**
 * “站点”可以是域名或 IP 地址。
 * 如果您遇到问题，请使用 Windows 控制面板来卸载所有 Array 程序，重新引导，然后重新连接。
 * 不适用于 Windows 8 RT。

## Linux 独立客户机

CentOS 64 位：https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat 32 位：https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat 64 位：https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32 位：https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64 位：https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. 使其成为可执行文件：`chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* 运行脚本：`./MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* 用法：`./MotionPro --host [site] --user [username] --passwd [password]`
* 使其停止：`[control-c]`

**注：**  
 * 要启动 MotionPro 客户机，必须至少输入 `hostname` 和 `username` 作为自变量。
 * “站点”可以是域名或 IP 地址。

## Mac OS X 10.10 独立客户机

针对 MacOS StandAlone Array SSL VPN Motion Pro Plus 客户机的步骤：

1. 从 Apple 商店安装“Motion Pro Plus”客户机。
* 在“应用程序”文件夹下找到 Motion Pro Plus 客户机，然后打开该应用程序。
* 单击“概要文件”，然后单击“添加”。
* 填写“站点名称”、“主机”和“用户名”，然后单击“确定”。
* 单击左上方的 VPN，然后进行连接。

示例见下图：

![图 1](images/snip20170425_1.png)

如果隧道未正确对流量定向，您可能需要[手动添加路径](https://discussions.apple.com/thread/2735376)。

*在更新之前，请卸载任何先前的版本。*

## SSL VPN POP（站点）

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


**请注意：在安装新版本之前，请先卸载客户机的任何先前版本。**

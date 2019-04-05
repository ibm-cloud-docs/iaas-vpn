---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: IPSec VPN, IP address, IP traffic

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 设置 IPSec VPN
{:#setup-ipsec-vpn}

## 什么是 IPSec VPN？
{:#what-is-ipsec-vpn}

IPSec 是一套协议，用于通过隧道方式（提供加密的站点到站点网络）来对两个位置之间的所有 IP 流量进行认证和加密。它只允许在网络上传递受信任数据，除此之外均视为不安全。有关 IPSec 的更多常规信息，请参阅[参考文档](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)。


通过 IBM Cloud 的 VPN 访问，用户可以使用 IBM Cloud 的专用网络来远程安全地管理所有服务器。通过建立从您的位置到专用网络的 VPN 连接，便可以使用加密的 VPN 隧道进行带外管理和服务器急救。通过 VPN 访问，您可以：

   * 通过 SSL 或 IPSEC 建立与专用网络的 VPN 连接
   * 通过 SSH 或 RDP 利用服务器的专用 10.x.x.x IP 地址来访问服务器
   * 连接到服务器的 IPMI IP 地址以满足其他服务器管理或急救需求。

我们提供的 IPSec 服务供客户用于管理其环境。建议不要将其用于生产工作负载。


## 设置 IPSec 连接
{:#setup-ipsec-connection}

### 协商参数
{:#setup-ipsec-vpn-negotiation-parameters}
![协商参数](images/IPSec_VPN.png)

您需要知道 IPSec VPN 远程端的以下信息：
- VPN 端点的静态 IP 地址
- 预共享密钥（密码）
- 加密算法（DES、3DES、AES128、AES192 和 AES256）
- 认证（MD5、SHA1 和 SHA256，对于阶段 1 和 2）
- Diffie-Hellman 组（对于阶段 1 和 2）
- 是否使用了完美前向保密 (PFS)？
- 关键生存时间（对于阶段 1 和 2）- **注：**我们的系统以秒为单位度量此值 !

一旦有了这些信息，就可以配置 VPN 连接的基本协商参数。

### 受保护的网络
{:#setup-ipsec-vpn-protected-networks}

在 VPN 连接属性中，必须在隧道的远程端以及隧道的本地网络上定义网络。在“受保护的客户（远程）子网”中，为 IPSec 隧道的远程（非 IBM）端输入以 CIDR 表示法表示的专用 IP 地址空间。

<span style="text-decoration: underline">例如：</span>如果隧道远程端的网络使用单个子网 10.0.0.0，网络掩码为 255.255.255.0，那么将为“受保护的客户（远程）子网”部分输入 IP 地址 10.0.0.0 / CIDR 24。

### 网络地址转换 (NAT)
{:#setup-ipsec-vpn-nat}

通过 IPSec VPN，您还可以在 {{site.data.keyword.BluSoftlayer_notm}} 网络上定义专用 IP 地址，用于将流量路由到 VPN 连接的另一端上的远程子网。这允许您将专用因特网流量转发到 VPN 后面的某台机器的其中一个内部 IP 地址，而不公开可完全访问因特网的远程位置。  

### 网络地址转换/分配的静态 NAT 子网
{:#setup-ipsec-vpn-nat-static-subnets}

要使用静态 NAT 条目配置远程 VPN IP，请执行以下操作： 

 * 选择红色箭头以在**分配的静态 NAT 子网**部分中显示子网列表。这将显示子网中的每个 IP。  
 * 在**客户 IP** 列下，输入 VPN 连接的远程端的 IP；在**名称**列下，输入映射的名称。  
 * 选择**添加/修改上下文地址转换**和**应用配置**，以保存并应用配置。
 
此操作为返回流量设置静态一对一网络转换，IBM Cloud VPN 集中器后面的主机将使用返回流量来与远程 VPN 同级后面的主机进行通信。例如，IP 10.1.255.92 的所有流量都将转换并转发给客户的 IP 192.168.10.15。此转发无需在 IBM Cloud 服务器上增加路由条目。

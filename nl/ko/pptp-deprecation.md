---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# PPTP VPN 지원 중단
{:#pptp-vpn-deprecation}

PPTP VPN은 2018년 6월 12일부터 지원이 중단되며 더 이상 고객에게 제공되지 않습니다. 관심을 가져주셔서 감사합니다. 가능한 대안에 관해 알아보려면 계속 읽으십시오.

## VPN의 개념
{:#pptp-vpn-deprecation-what-is-vpn}
사용자는 VPN 액세스를 사용하여 IBM Cloud 사설 네트워크를 통해 모든 서버를 원격으로 안전하게 관리할 수 있습니다. 사용자 위치에서 사설 네트워크로의 VPN 연결은 암호화된 VPN 터널을 통한 대역 외 관리 및 서버 복구를 허용합니다. VPN 액세스를 사용하여 다음을 수행할 수 있습니다.

* SSL, **PPTP** 또는 IPSec를 통해 사설 네트워크에 대한 VPN 연결 설정
* SSH 또는 RDP를 통해 사설 10.x.x.x IP 주소를 사용하여 서버에 액세스
* 추가 서버 관리 또는 복구 요구사항을 위해 서버의 IPMI IP 주소에 연결

## PPTP 지원 중단
{:#pptp-deprecation-vpn}
다른 VPN 옵션이 더 안전하고 다양해짐에 따라 PPTP에 대한 필요성이 감소되었습니다. {{site.data.keyword.BluSoftlayer_notm}}는 PPTP보다 더 정교하고 보호적인 SSL 또는 IPSec와 같은 몇 가지 다른 옵션을 제공합니다.

**이러한 이유로 2018년 6월 12일부터 {{site.data.keyword.BluSoftlayer_notm}}에서 PPTP를 더 이상 제공하지 않습니다.**
{:important}


## 자주 질문되는 내용(FAQ)
{:#pptp-vpn-deprecation-faq}

**Q: PPTP가 지원 중단되는 이유는 무엇입니까?**

**A:** {{site.data.keyword.BluSoftlayer_notm}}에서는 최고 품질의 보호를 제공하기 위해 PPTP의 사용을 중단했습니다. {{site.data.keyword.BluSoftlayer_notm}}는 개인정보와 데이터의 보안이 가장 중요하다는 고객과의 약속을 지키려고 합니다. 

**Q: PPTP 이외에 사용 가능한 다른 VPN 액세스 유형은 무엇입니까?**

**A:** {{site.data.keyword.BluSoftlayer_notm}}는 단순 구성만 필요한 몇 가지 옵션을 제공합니다.
  1. SSL VPN은 브라우저로부터 직접 사설 네트워크에 연결하는 빠른 액세스 연결입니다. SSL VPN은 Windows XP 이상 및 ActiveX, Fedora, Ubuntu 및 Mac OSX와 호환 가능합니다. 사설 네트워크에 대한 글로벌 액세스는 단일 URL에서 사용 가능하므로, 가장 가까운 VPN 엔드포인트를 선택할 수 있습니다. 이 옵션을 시작하는 데 대한 세부사항은 [SSL VPN 연결 설정](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections)을 참조하십시오.
  2. IPSec는 두 위치 사이의 모든 IP 트래픽을 인증하고 암호화하도록 디자인된 프로토콜 모음입니다. 보안 데이터가 비보안으로 간주될 수 있는 네트워크를 통해 이동하도록 허용합니다. IPSec에 대한 자세한 일반 정보는 [IPSec VPN 설정](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) 및 이 서비스 사용을 시작하기 위한 기타 [참조 문서](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)를 참조하십시오. 

**Q: 내 비즈니스 업무에 PPTP가 필요한 경우 어떻게 합니까?**

**A:** PPTP가 비즈니스 요구사항에 필요한 경우 몇 가지 옵션을 사용할 수 있습니다. **가능한 모든 옵션이 여기에 포함되어 있지는 않습니다. 다음 옵션을 사용하려면 두 엔드포인트 모두의 전체 구성이 필요하다는 점에 주의하십시오. 이러한 옵션의 구성은 고객의 책임입니다.**
  1. 가상 라우터 어플라이언스. Vyatta라고도 하는 가상 라우터 어플라이언스는 환경에 대한 게이트웨이 및 라우터 역할을 합니다. 여기에는 서브넷으로 구성된 구역이 포함됩니다. 서로 통신할 수 있도록 구역 간에 방화벽 규칙이 설정됩니다. 다른 구역과 통신할 필요가 없는 구역의 경우 모든 패킷이 삭제되기 때문에 방화벽 규칙이 필요하지 않습니다. 이 서비스를 시작하는 데 대한 세부사항은 [가상 라우터 어플라이언스 시작하기](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance)를 참조하십시오. 
  2. FSA 방화벽. FortiGate 보안 어플라이언스(FSA) 10Gbps는 공용 및 사설 네트워크 둘 다를 위해 다중 VLAN의 트래픽을 보호하도록 구성할 수 있는 하드웨어 방화벽입니다. 고객 포털에서는 "다중 VLAN 방화벽"이라고도 합니다. 이 서비스를 시작하는 데 대한 세부사항은 [FSA 10Gbps 시작하기](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps)를 참조하십시오. 
 
이전 옵션은 {{site.data.keyword.BluSoftlayer_notm}}에서 더 이상 서비스를 제공하지 않게 된 후 PPTP가 비즈니스 요구사항에 필요한 경우에 탐색할 수 있는 몇 가지 가능성입니다. 보내주신 성원에 감사드립니다.{:note}

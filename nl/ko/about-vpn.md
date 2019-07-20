---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# VPN 정보
{:#about-iaas-vpn}

VPN 액세스를 사용하면 IBM Cloud 사설 네트워크를 통해 원격으로 사용자 계정과 연관된 모든 서버 및 서비스를 관리할 수 있습니다. 사용자 위치에서 사설 네트워크로의 VPN 연결은 암호화된 VPN 터널을 통한 **대역 외 관리 및 서버 복구**를 허용합니다.

사설 네트워크를 사용한 통신이 본질적으로 더 안전합니다. 여전히 서버를 관리할 수 있으면서도 공용 액세스를 제한하는 유연성을 제공합니다. 계정의 모든 사용자에게 VPN 액세스 권한이 제공될 수 있으며, SSL로 사용 가능합니다. [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)을 통한 VPN 상호작용은 사용자 레벨에서 VPN 액세스 사용자 정의를 허용합니다.

## SSL VPN을 사용하는 몇 가지 방법은 무엇입니까?
{:#ways-to-use-iaas-vpn}

이 대역 외 보안 게이트웨이는 사설 네트워크를 통한 서버 액세스를 제공합니다. 일반적인 사용법은 다음과 같습니다.

* SSH 또는 RDC의 경우 서버의 사설 IP 주소(10.x.x.x)에 연결합니다.
* 원격 콘솔/액세스/모니터링을 위해 IPMI 카드에 연결합니다.
* 편의성을 위해 홈 또는 작업 PC에서 Windows 또는 Red Hat의 드라이브를 마운트합니다.
* 데이터베이스 서버의 공용 인터페이스를 시스템 종료하고 사설 네트워크를 통해 관리합니다.
* 처음으로 서버를 설정하는 동안 공용 인터페이스를 시스템 종료합니다.
* 중요 보안 업데이트 동안 공용 인터페이스를 시스템 종료합니다.
* 보안 위반 중에 공용 인터페이스를 시스템 종료하고 사설 네트워크를 통해 문제를 해결합니다.

## 주요 기능
{:#iaas-vpn-key-features}

 * 사설 네트워크는 무료로 서버와 통신하고 서버를 관리하는 방법을 제공합니다. VPN은 이 사설 네트워크에 대한 게이트웨이입니다.
 * 가능한 한 전 세계에서 액세스 지점이 가장 좋고 빠른 액세스 및 상호작용을 작성합니다. IBM Cloud는 현재 많은 도시에 VPN 액세스 지점을 갖고 있습니다.
 * {{site.data.keyword.BluSoftlayer_notm}} 사설 네트워크에 대한 VPN 액세스 지점의 목록에 대해서는 http://www.softlayer.com/vpn-access 를 방문하십시오.

## 작동 방식
{:#iaas-vpn-how-it-works}

VPN 액세스를 사용하는 경우 SSL을 사용하여 사설 네트워크로 연결하고 서버 및 서비스를 관리하십시오. 

## SSL VPN 연결
{:#iaas-vpn-ssl-vpn-connections}

SSL VPN은 브라우저로부터 직접 사설 네트워크에 연결하는 빠른 액세스 연결입니다. SSL VPN은 Windows XP 이상 및 ActiveX, Fedora, Ubuntu 및 Mac OSX와 호환 가능합니다. 사설 네트워크에 대한 글로벌 액세스는 단일 URL에서 사용 가능하므로, 가장 가까운 VPN 엔드포인트를 선택할 수 있습니다.

## SSL VPN 서브넷 한계
{:#iaas-vpn-ssl-vpn-subnet-limit}

SSL VPN 클라이언트는 라우팅 테이블을 채우는 데 사용할 수 있는 견고한 64-서브넷 한계를 갖고 있습니다. 계정이 64개가 넘는 서브넷을 갖고 있는 경우 수동 서브넷 지정을 사용하도록 SSL VPN 권한을 수정해야 합니다. 그렇지 않는 경우 일부 서브넷이 SSL VPN을 통해 도달 불가능하게 될 수 있습니다.

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, IBM Cloud VPN, user account

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# VPN(Virtual Private Network) 시작하기
{:#gettingstarted-with-virtual-private-networking}

## IBM Cloud VPN이란 무엇입니까?
{:#what-is-ibmcloud-vpn}


사용자는 VPN 액세스를 사용하여 IBM Cloud 사설 네트워크를 통해 모든 서버를 원격으로 안전하게 관리할 수 있습니다. 사용자 위치에서 사설 네트워크로의 VPN 연결은 암호화된 VPN 터널을 통한 대역 외 관리 및 서버 복구를 허용합니다. VPN 액세스를 사용하여 다음을 수행할 수 있습니다.

* SSL 또는 IPSec를 통해 사설 네트워크에 대한 VPN 연결 설정
* SSH 또는 RDP를 사용하여 사설 10.x.x.x IP 주소를 통해 서버에 액세스
* 추가 서버 관리 또는 복구 요구를 위해 서버의 IPMI IP 주소에 연결

**[공지사항](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)에 설명된 대로 2018년 6월 12일부터 PPTP VPN 서비스가 더 이상 사용되지 않습니다.**
{:deprecated}

많은 서비스는 사설 네트워크를 통해 액세스가 필요하며, VPN은 사설 네트워크 액세스를 허용하는 한 가지 방법입니다. VPN은 사설 네트워크에 로그인하고 작업을 수행한 후 로그아웃해야 할 때 사용하기에 좋습니다. 예를 들어, 이 액세스는 종종 서버의 KVM에 접근하기 위해 필요합니다.

각 사용자 계정은 VPN 액세스 권한이 제공되고 액세스가 필요한 서브넷에 관하여 제한될 수 있습니다. VPN 액세스가 사용 가능해야 하며 VPN에 로그인할 수 있으려면 먼저 VPN 비밀번호를 작성해야 합니다.

## 각 사용자의 VPN 액세스 사용 설정
{:#enable-user-vpn-access}

시작하려면 VPN 액세스가 필요한 각 계정에서 VPN 액세스를 사용으로 설정해야 합니다. 팀의 마스터 계정을 포함한 모든 계정은 VPN 액세스 **사용 안함**으로 시작합니다. VPN 액세스를 사용으로 설정하려면 다음 단계를 수행하십시오.

1. [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)에서 **계정 -> VPN 액세스**로 이동하십시오.
* **VPN 액세스** 열에서 각 가능한 VPN 사용자 및 연결에 대한 행을 찾을 수 있습니다.
* 사용자가 아직 VPN 액세스를 사용으로 설정되지 않은 경우 연결은 "없음"으로 표시됩니다.
* 사용자의 VPN 액세스 연결이 **SSL**로 표시되면 이미 VPN 액세스가 사용으로 설정되었음을 의미합니다.

![Softlayer 포털 VPN 액세스 표](images/vpnaccess01.png)

1. 특정 사용자에게 허용되는 VPN 액세스 유형을 사용으로 설정하거나 변경하려면 **VPN 액세스** 열의 연결을 클릭하십시오.
* 다음 페이지에서 각 사용자에 대해 적합한 VPN 액세스 유형을 사용으로 설정할 수 있습니다.  

![사용자에게 VPN 유형 액세스 지정](images/vpntype01.png)

## VPN 비밀번호 설정
{:#set-vpn-password}

다음 단계는 VPN 비밀번호를 작성하는 것입니다. 각 사용자는 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)에서 VPN 비밀번호를 작성 및 업데이트할 수 있습니다. 그렇게 하려면 맨 위 오른쪽에서 이름을 선택하십시오. **프로파일 편집** 페이지로 이동하게 됩니다. 또한 **계정 -> 사용자**를 선택한 후 사용자 이름을 선택할 수도 있습니다.

      참고: 연결은 "마스터 사용자"로 표시됩니다. 이 연결은 하위 사용자에게 대해 사용자 이름을 읽습니다.

**사용자 프로파일 편집** 페이지에서, 아래로 스크롤하여 VPN 비밀번호를 초기화 또는 업데이트하십시오.

![프로파일 VPN 비밀번호 편집 필드](images/vpnpasswordfields.png)

## VPN 로그인
{:#login-to-the-vpn}

VPN 액세스가 설정되었으므로 로그인할 수 있습니다.

1. SSL VPN에 로그인하려면 [vpn.softlayer.com](https://vpn.softlayer.com/)에서 로그인 지점을 선택하십시오. 임의의 VPN 액세스 지점을 사용할 수 있으며, 모든 데이터 센터의 사설 네트워크에 대한 동일한 액세스 권한이 부여됩니다.
* 한 위치에 로그인하는 데 문제가 있으면 다른 위치를 시도하십시오.
* 다른 방법으로는, 독립형 클라이언트 SSL VPN을 사용하여 로그인할 수 있습니다.

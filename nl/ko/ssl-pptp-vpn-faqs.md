---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# VPN FAQ
{:#vpn-faq}

## IBM Cloud VPN이란 무엇입니까?
{:#what-is-ibm-cloud-vpn}
{:faq}

IBM Cloud VPN 액세스는 사용자가 IBM Cloud 사설 네트워크를 통해 모든 서버를 안전하게 원격으로 관리할 수 있도록 디자인되었습니다.  사용자 위치에서 사설 네트워크로의 VPN 연결은 대역 외 관리 및 암호화된 VPN 터널을 통한 서버 복구를 허용합니다. VPN 액세스를 사용하여 다음을 수행할 수 있습니다.

* SSL 또는 IPSEC를 사용한 사설 네트워크로의 VPN 연결 설정
* SSH 또는 RDP를 사용한 사설 10.x.x.x IP 주소를 통해 서버 액세스
* 추가 서버 관리 또는 복구 요구를 위해 서버의 IPMI IP 주소에 연결


## SSL VPN이 PPTP, IPSEC 또는 기타 VPN 프로토콜도 수행합니까?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

현재로서는 SSL VPN 게이트웨이는 브라우저 기반 SSL VPN 플러그인 또는 연결 작성을 위한 등록 클라이언트를 사용합니다. 계속해서 더 많은 VPN 연결 옵션을 사설 네트워크에 추가할 예정입니다. SSL VPN은 사용 편의성과 호환성을 위해 선택되었습니다. PPTP는 더 이상 사용되지 않습니다. 자세한 정보는 [PPTP VPN 지원 중단](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)을 참조하십시오.



## SSL VPN 게이트웨이를 통해 내 원격 위치에서 NAS/FTP 서버를 마운트할 수 있습니까?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

아니오. SSL VPN 게이트웨이에서 사설 VLAN 및 서버에만 액세스할 수 있습니다. NAS/FTP 볼륨에서 데이터를 다운로드하려는 경우, 데이터를 서버로 이동한 후 VPN을 통해 원격 위치로 다시 이동해야 합니다.

보안상의 이유로, 데이터 센터 내부에 있는 서버만 서비스(DNS, 업데이트, NAS, Lockbox)를 제공하는 서버에 액세스할 수 있습니다.


## 어떤 공급업체가 SSL VPN을 제작하며 어떻게 작동합니까?
{:#what-vendor-makes-ssl-vpn}
{:faq}

SSL VPN 게이트웨이는 Array Networks의 보안 제품입니다.  게이트웨이 자체는 고객 포털의 사용자 및 비밀번호를 업데이트하기 위해 반경을 그립니다. 사용자를 추가하고 SSL VPN 액세스 권한을 부여하려는 경우, 고객 포털 내부에 새 사용자를 작성하고 SSL VPN 권한을 사용하도록 설정하십시오.


## SSL과 PPTP VPN 사이의 차이점은 무엇입니까?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL VPN**에서는 사용자가 원격 데스크탑에서 {{site.data.keyword.BluSoftlayer_notm}} 사설 네트워크로의 보안 터널을 작성할 수 있습니다. 다양한 운영 체제와 호환 가능합니다.

**PPTP VPN**에서는 동일한 보안 터널이 허용되지만 사용자 데스크탑 또는 데디케이티드 디바이스에서 특화된 클라이언트 소프트웨어를 사용하여 연결합니다. 그러나 PPTP는 더 이상 사용되지 않습니다. 자세한 정보는 [PPTP VPN 지원 중단](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)을 참조하십시오.

## PPTP VPN에 대한 추가 사용자를 추가할 수 없는 이유는 무엇입니까?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP는 더 이상 사용되지 않습니다. 자세한 정보는 [PPTP VPN 지원 중단](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation)을 참조하십시오.

## 고객 포털 내에서 사용자의 VPN 관리 상태에 대해 사용 가능한 카테고리는 무엇입니까?
{:#what-are-available-categories-vpn-management}
{:faq}

고객 상태 카테고리에는 사용자가 업데이트할 수 있는 것과 자동으로 나타날 수 있는 것이 포함됩니다. 다음이 포함됩니다.

* **활성** - 사용자가 계정 관리자가 설정한 권한을 바탕으로 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 및 VPN에 액세스할 수 있습니다. 이 상태는 언제든지 수동으로 선택하거나 변경될 수 있습니다.
* **사용 안함** - 사용자가 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 및 VPN을 포함하여 계정의 모든 권한이나 구독에 액세스할 수 없습니다. 계정의 다른 사용자에 의해 사용 안함으로 설정되는 경우 이 상태는 언제든지 수동으로 선택 및/또는 변경될 수 있습니다.
* **VPN 전용** - 사용자는 VPN 연결에만 액세스할 수 있으며 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)에 액세스할 수 없습니다. 이 상태는 언제든지 수동으로 선택하거나 변경될 수 있습니다.
* **비활성** - 사용자가 지난 60일 동안 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 또는 VPN을 이용하지 않았습니다. 이것은 시스템이 생성한 상태입니다.
* **취소 보류 중** - 계정 관리자가 이 사용자를 취소했고 취소가 현재 처리되는 중입니다. 이 상태는 시스템이 생성한 상태입니다.

## SSL VPN 설정 방법
{:#how-do-i-set-up-ssl-vpn}
{:faq}

자세한 지시사항은 [SSL VPN에 연결 - Windows 7 이상](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7)을 참조하십시오.



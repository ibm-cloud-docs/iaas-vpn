---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL VPN에 연결 - Windows 7 이상
{:#connect-ssl-vpn-windows7}

{{site.data.keyword.BluSoftlayer_notm}} SSL VPN에 연결하려면 사용자 컴퓨터에서 몇 가지 단계를 수행하여 연결 기능을 보장해야 할 수 있습니다.

**1. 제어판에서 사용자 액세스 제어(UAC) 끄기**

1. **시작 -> 제어판 -> 사용자 계정 -> 사용자 계정 제어 설정 변경**으로 이동하십시오.
* **컴퓨터 보호를 돕기 위해 사용자 계정 제어(UAC) 사용** 옆에 있는 상자를 **선택 취소**하십시오.

**2. 관리자 계정 사용 설정**

1. **시작 -> 제어판 -> 관리 도구 -> 컴퓨터 관리 -> 로컬 사용자 및 그룹 -> 사용자 ->**로 이동하십시오. 
* **관리자** 사용자를 마우스 오른쪽 단추로 클릭하고 **특성**을 선택하십시오. 
* **계정 사용 안함**에 대한 상자를 선택 취소하십시오.

**3. SSL VPN 페이지에 연결하기 전에 관리자로서 Internet Explorer 실행**

1. Internet Explorer 아이콘을 마우스 오른쪽 단추로 클릭하고 메뉴에서 **관리자로서 실행**을 선택하십시오.

이전 단계가 완료된 후에는 로그인할 수 있어야 합니다. 

## 로그인
{:#connect-windows-login}

1. [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access)로 이동하고 포털 사용자 이름 및 비밀번호를 사용하여 로그인하십시오. 
* 사용자가 [SSL VPN 액세스 권한을 가져야](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user) 합니다.  
* 또한, VPN 비밀번호를 설정했어야 합니다. 그렇게 하려면 [사용자 프로파일 페이지](https://control.softlayer.com/account/user/profile)를 업데이트하고 **VPN 비밀번호**를 나타내는 상자를 채우십시오.

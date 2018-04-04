---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Windows 10에서 PPTP VPN 설정

1. **시작** 메뉴에서 **설정** 애플리케이션을 실행하고 **네트워크 및 인터넷**을 클릭하십시오. 

2. **네트워크 및 인터넷** 패널의 왼쪽에서 **VPN**을 선택하고, 후속 페이지에서 **VPN 연결 추가**를 선택하십시오. 

![VPN 연결 추가](images/vpn1.png)

3. 다음 페이지에서 PPTP VPN 연결을 설정합니다. 설정은 다음과 같습니다. 

 * _VPN 제공자:_ Windows(기본 제공)
 * _연결:_ 이 연결에 이름을 제공해야 합니다(예: `MyPPTP`). 
 * _서버 이름 또는 주소:_ 접근하려는 서버의 이름을 입력하십시오. (예: `pptpvpn.dal01.softlayer.com`)
 * _VPN 유형:_ "Point to Point Tunneling Protocol"(PPTP)을 선택하십시오.
 *_ 로그인 유형:_ "사용자 이름 및 비밀번호"를 선택하십시오. 
  * 이제 VPN 사용자 이름 및 비밀번호를 입력하십시오. 
  * 모든 선택된 데이터를 다시 한 번 확인하고 **저장**을 누르십시오. 

![VPN 설정](images/vpn2.png)

4. 기본 VPN 페이지로 돌아온 후, `MyPPTP` 연결(이전에 작성한)을 선택하여 연결하십시오. 

![Softlayer PPTP](images/vpn3.png)

5. 연결된 중에 인터넷을 사용하려면 원격 게이트웨이를 사용 안함으로 설정해야 합니다. 이것은 PowerShell을 통해 수행할 수 있습니다. 

 * PowerShell을 마우스 오른쪽 단추로 클릭하고 **관리자로서 실행**을 선택하여 PowerShell을 여십시오. 
 * 다음 명령을 입력하십시오. 
 ```
`Get-VpnConnection`
`Set-VpnConnection -Name "MyPPTP" -SplitTunneling $True`
```

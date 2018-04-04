---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mac OS X 10.X에 대한 PPTP VPN 설정

PPTP VPN 연결은 데스크탑이나 데디케이티드 디바이스로부터 {{site.data.keyword.BluSoftlayer_notm}} 사설 네트워크로의 원격 연결을 허용합니다. PPTP를 통한 사설 네트워크 연결은 Mac OS X를 포함한 다중 운영 체제에 사용 가능합니다. 사용자는 설정 시에 데이터 센터의 고유한 목적지 주소를 입력하여 모든 {{site.data.keyword.BluSoftlayer_notm}} 데이터 센터에 연결할 수 있습니다. Mac OS X에서 PPTP VPN 연결을 설정하려면 다음 단계를 따르십시오. 

## PPTP VPN 연결 설정

* **Apple 메뉴** 드롭 다운에서 **시스템 환경 설정**을 선택하십시오. 
* 인터넷&네트워크 섹션에서 **네트워크** 아이콘을 클릭하십시오. 
* **연결** 메뉴의 맨 아래에 있는 **더하기 부호** 아이콘을 클릭하십시오. VPN 연결을 작성할 수 있는 팝업 상자가 나타납니다. 
* VPN 연결을 작성하십시오. 
  * **인터페이스** 드롭 다운 목록에서 **VPN**을 선택하십시오. 
  * **VPN 유형** 드롭 다운 목록에서 **PPTP**를 선택하십시오. 
  * **서비스 이름** 필드에 연결에 대한 **설명식 제목**을 입력하십시오. 
  * **참고:** 데이터 센터 위치를 서비스 이름의 일부로 사용할 것을 권장합니다. 
  * **작성** 단추를 클릭하십시오. 
* 연결 메뉴에서 방금 작성한 연결을 클릭하십시오. 
* **서버 주소** 필드에 원하는 데이터 센터의 **목적지 주소**를 입력하십시오. 현재 {{site.data.keyword.BluSoftlayer_notm}} 데이터 센터에 대해 적절한 주소는 아래의 표를 참조하십시오. 
* **계정 이름** 필드에 **고객 포털 사용자 이름**을 입력하십시오. 
* 인증 설정을 완료하십시오. 
  * **인증 설정** 단추를 클릭하십시오. VPN의 인증을 프롬프트하는 팝업 상자가 나타납니다. 
  * **비밀번호** 필드에 **고객 VPN 비밀번호**를 입력하십시오. 
  * **확인** 단추를 클릭하십시오. 
* VPN 트래픽 설정을 업데이트하십시오. 
  * **고급** 단추를 클릭하십시오. 
  * 세션 섹션의 **VPN 연결을 통해 모든 트래픽 전송** 선택란이 선택되지 않았는지 확인하십시오. 
  * **확인** 단추를 클릭하십시오. 
* **메뉴에 VPN 상태 표시** 선택란을 선택하십시오. 
* 적용 단추를 클릭하십시오. 이제 VPN 메뉴 표시줄 항목을 사용하여 언제든지 VPN 연결을 구축할 수 있습니다. 

|데이터 센터 위치|데이터 센터 인터넷 주소|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapore, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, HK|pptpvpn.hkg02.softlayer.com|
|Melbourne, AU|pptpvpn.mel01.softlayer.com|
|London, GB|pptpvpn.lon02.softlayer.com|
|Paris, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokyo, JP|pptpvpn.tok02.softlayer.com|

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Windows 7에 대한 PPTP VPN 설정

PPTP VPN 연결은 데스크탑이나 데디케이티드 디바이스로부터 {{site.data.keyword.BluSoftlayer_notm}} 사설 네트워크로의 원격 연결을 허용합니다. PPTP를 통한 사설 네트워크 연결은 Windows 7을 포함한 다중 운영 체제에 사용 가능합니다. 사용자는 설정 중에 데이터 센터의 고유한 목적지 주소를 입력하여 모든 {{site.data.keyword.BluSoftlayer_notm}} 데이터 센터에 연결할 수 있습니다. Windows 7에서 PPTP VPN 연결을 설정하려면 아래 단계를 따르십시오. 

## PPTP VPN 연결 설정

1. 원격 연결을 설정하는 화면으로 이동하려면 Microsoft의 [사용 방법 페이지](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window}를 참조하십시오. 

2. 인터넷 주소 필드에 원하는 데이터 센터의 목적지 주소를 입력하십시오. 현재 IBM Cloud 데이터 센터에 대한 적절한 주소에 대해서는 아래의 표를 참조하십시오. 

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

3\. **목적지 이름** 필드에 연결의 식별 이름을 입력하십시오. 

**참고:** 데이터 센터 위치를 목적지 이름으로 사용할 것을 권장합니다. 

4\. **사용자 이름** 필드에 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 사용자 이름을 입력하십시오. 

5\. **비밀번호** 필드에 **VPN 비밀번호**를 입력하십시오. 

6\. **연결** 단추를 클릭하십시오. 

7\. 이제 컴퓨터에서 인터넷뿐 아니라 VPN에 연결할 수 있도록 원격 게이트웨이를 사용하지 않도록 설정해야 합니다. 

8\. **시작**을 클릭한 후, **제어판** -> **네트워크 및 공유** -> **어댑터 설정 변경**을 여십시오. 

9\. PPTP VPN 연결을 마우스 오른쪽 단추로 클릭하고 **특성**을 클릭하십시오. 

10\. TCP/IPv6 상자를 선택 취소한 후 TCP/IPv4와 특성을 차례로 클릭하십시오. 

11\. **고급** 단추를 클릭하십시오. 

12\. **원격 네트워크에서 기본 게이트웨이 사용** 상자를 선택 취소한 후 **확인**을 선택하십시오. 

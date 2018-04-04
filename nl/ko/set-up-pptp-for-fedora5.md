---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Fedora Core 5에 대한 PPTP 설정

설치 및 구성하는 방법입니다. 

**1. 설치**
다음 명령 중 하나를 사용하여 PPTP 및 `pptpconfig` GUI를 설치하십시오. 
```
# rpm -Uvh http://pptpclient.sourceforge.net/yum/stable/fc5/pptp-release-current.no...
# yum --enablerepo=pptp-stable install pptpconfig
```

**2. 구성**

1. IBM Cloud PPTP 정보:
<table><tr><td>서버:</td><td>pptpvpn.dal01.softlayer.com (Dallas)<br/>pptpvpn.sea01.softlayer.com (Seattle)<br/>pptpvpn.wdc01.softlayer.com (Washington D.C.)</td></tr><tr><td>도메인 이름:</td><td>공백으로 둠</td></tr><tr><td>사용자 이름:</td><td>(예: SL12345)</td></tr><tr><td>비밀번호:</td><td>&nbsp;</td></tr></table>

2. *pptpconfig*를 <span style="text-decoration: underline">루트로서</span> 실행하십시오. 창이 나타납니다. <br/>
![그림 1](images/ss1.jpeg)

3. 서버 탭에 이름, 서버, 사용자 이름 및 비밀번호를 입력하십시오. 

4. 암호화 섹션에서 대부분의 고객에 대해 작동하도록 모든 것을 기본값으로 두십시오. <br/>
![그림 2](images/ss2.jpeg)

5. *추가*를 클릭하십시오. 터널이 목록에 나타납니다. 

6. 터널을 클릭하여 선택하고 *시작*을 클릭하십시오. 터널 연결 로그 및 상태를 갖는 창이 나타납니다. 

7. 연결이 실패하면 추가 정보를 수집해야 할 수 있으므로, *기타* 탭에서 *연결 디버깅 기능 사용 설정*을 클릭하고 *업데이트*를 클릭하고, *시작*을 다시 시도한 후 표시되는 모든 오류에 대한 [진단 HOWTO](http://pptpclient.sourceforge.net/howto-diagnosis.phtml){:new_window}를 보십시오. <br/>
![그림 3](images/ss3.jpeg)

8. 연결이 성공한 경우 Ping 테스트 단추를 시도할 수 있습니다. Ping이 실패하면 계속하기 전에 이유를 찾으려고 시도해야 합니다. Ping이 작동하는 경우 터널이 활성 상태이며 이제 라우팅에 대해 작업할 수 있습니다. 

9. IBM Cloud의 백엔드 네트워크에서 살아있는 IP만이 이 VPN 터널을 지나 라우트되어야 합니다. 터널을 *중지*하고, 다시 선택한 후, *라우팅* 탭에서 *클라이언트 대 LAN 또는 LAN 대 LAN* 중 하나를 클릭하고 *네트워크 라우트 편집* 단추를 사용하여 네트워크에 대해 '10.0.0.0/8' 및 이름에 대해 'SoftLayer'를 입력한 후 다시 *시작*을 시도하십시오. 이제 10.0.80.11에 있는 사용자 서버의 사설 IP 주소 또는 SoftLayer의 사설 이름 서버에 액세스해 보십시오. <br/>
![그림 4](images/ss4.jpeg)

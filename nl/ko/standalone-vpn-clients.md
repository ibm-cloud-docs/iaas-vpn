---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 독립형 VPN 클라이언트 - Windows, Linux 및 Mac OS X

## Windows 독립형 클라이언트

Windows(8/7/Vista/XP) 32비트:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows(8/7/Vista/XP) 64비트:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. 운영 체제에 따라서 위에 나열된 파일 중 하나를 다운로드하십시오. 
* MotionProSetup을 실행하여 소프트웨어를 설치하십시오. 
* MotionPro를 실행하고 열린 화면에서 **프로파일 -> 추가**를 선택하십시오. 
* 사이트 이름을 제공하고 SSL VPN 사이트의 목록(아래)에서 호스트 이름을 선택하여 프로파일을 작성하십시오. 그런 다음 VPN 사용자 이름과 비밀번호를 입력하고 **저장**을 누르십시오. 
* 마지막으로, 방금 작성한 프로파일을 두 번 클릭하여 VPN에 연결하십시오. 

**참고**
 * '사이트'는 도메인 이름 또는 IP 주소일 수 있습니다. 
 * 문제가 있으면 Windows 제어판을 사용하여 모든 Array 프로그램을 설치 제거하고 다시 부팅한 후 다시 연결하십시오. 
 * Windows 8 RT에서는 작동하지 않습니다. 

## Linux 독립형 클라이언트

CentOS 64비트: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat 32비트: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat 64비트: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32비트: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64비트: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. 실행 가능하게 만드십시오. `chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* 스크립트를 실행하십시오. `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh.`
* 사용법:  `./MotionPro --host [site] --user [username] --passwd [password]`
* 중지하려면 `[control-c]`를 사용하십시오. 

**참고:**  
 * MotionPro 클라이언트를 시작하려면 최소한 `hostname` 및 `username`을 인수로 입력해야 합니다. 
 * '사이트'는 도메인 이름 또는 IP 주소일 수 있습니다. 

## Mac OS X 10.10 독립형 클라이언트

MacOS 독립형 어레이 SSL VPN Motion Pro Plus 클라이언트에 대한 단계:

1. Apple 스토어로부터 "Motion Pro Plus" 클라이언트를 설치하십시오. 
* 애플리케이션 폴더에서 Motion Pro Plus 클라이언트를 찾아서 애플리케이션을 여십시오. 
* '프로파일'을 클릭한 후 '추가'를 클릭하십시오. 
* 사이트 이름, 호스트 및 사용자 이름을 채운 후 확인을 클릭하십시오. 
* 맨 위 왼쪽에 있는 VPN을 클릭한 후 연결하십시오. 

다음에서 예를 확인할 수 있습니다. 

![그림 1](images/snip20170425_1.png)

터널이 트래픽을 올바르게 지시하지 않을 경우 [라우트를 수동으로 추가](https://discussions.apple.com/thread/2735376)해야 할 수 있습니다. 

*업데이트하기 전에 모든 이전 버전을 설치 제거하십시오. *

## SSL VPN POP(사이트)

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


**새 버전을 설치하기 전에 클라이언트의 모든 이전 버전을 설치 제거해야 합니다. **

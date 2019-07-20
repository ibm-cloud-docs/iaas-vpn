---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Linux Fedora, SSL VPN connections Windows, backend IP address

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# SSL VPN 연결 설정
{:#setup-ssl-vpn-connections}

Windows, Linux Fedora 및 Linux는 개별화된 연결 지시사항이 이 문서에 표시되어 있습니다. 다음은 SSL VPN 연결을 사용할 수 있는 방법의 몇 가지 예입니다.

* Windows 2003 서버의 관리를 위한 서버의 백엔드 IP 주소(10.4.X.X)로의 원격 데스크탑.
* UNIX 서버 관리를 위한 서버의 백엔드 IP 주소(10.4.X.X)로의 SSH.
* 백엔드 IPMI 주소(10.4.X.X)를 사용하여 서버를 제어하려면 IPMI 클라이언트를 사용하십시오. http://downloads.softlayer.local/ipmi/ 로 이동하여 연결되고 나면 IPMI 클라이언트 도구를 다운로드할 수 있습니다(SoftLayer Private VPN에 연결되어야 함).
  * **참고:** IPMIView는 Java가 설치되어야 합니다.  http://www.sun.com/java/
* 공인 IP에서 작동하도록 만들기 전에 백엔드 IP에서 웹 사이트 테스트.
* 사용자 서버와 홈/사무실 사이의 안전한 데이터의 파일 전송.
* 홈/사무실로 서버의 구성 파일 백업.
* [웹 포털](http://control.softlayer.com/)에 안전하게 연결하십시오.

## Windows(Internet Explorer)
{:#setup-ssl-vpn-connections-windows}

1. Internet Explorer를 열고 `http://www.softlayer.com/vpn-access`로 이동하십시오.
* 사용자 이름과 비밀번호를 입력한 후에 ActiveX 플러그인을 설치하라는 프롬프트가 표시됩니다. 백엔드 네트워크에 연결하려면 이 플러그인을 설치해야 합니다. 
* 또한 ActiveX 플러그인을 설치하려면 워크스테이션에서 관리 권한이 있어야 합니다. 플러그인 설치 권한이 없으면 로컬 시스템 관리자에게 플러그인을 설치해 줄 것을 요청하십시오. 
* ActiveX 플러그인이 설치되면 어레이 SSL VPN 네트워크 커넥터가 실행되고 VPN 디바이스에 대한 연결을 구축합니다. 성공하는 경우 빨간색 '**A**'가 작업 표시줄에 나타납니다. 언제든지 '**A**'를 클릭하여 SSL VPN 연결의 상태(상태, 지정된 IP 주소, 지정된 DNS 서버, 네트워크 라우트, 연결된 시간)를 볼 수 있습니다. 
* 언제든지 브라우저 세션을 최소화하고 사설 네트워크에서 다른 애플리케이션을 안전하게 계속 사용할 수 있습니다. 
* 완료한 후에는 오른쪽의 연결 끊기 단추를 선택하여 연결을 끊거나 단순히 창을 닫으십시오.

## Linux Fedora 
{:#setup-ssl-vpn-connections-linux}

Firefox에서 더 이상 NPAPI 플러그인을 지원하지 않습니다(Java 애플릿). 다른 브라우저를 사용하여 이 단계를 수행하십시오.
{:note}

모든 명령을 루트로서 실행할 것을 권장합니다. (`setuid root`)

1. `http://java.com/en/download/manual.jsp`에서 Java를 다운로드하십시오. 이것은 Linux 자체 추출 파일입니다.
* 브라우저를 닫으십시오.
* 파일을 Java를 설치할 장소(대개 `/usr/local`에 있음)로 이동하십시오.
* `chmod +x jre-6u1-linux-i586.bin` 명령을 사용하여 파일을 실행 가능하게 만드십시오.
* `./jre-6u1-linux-i586.bin` 명령을 사용하여 설치 프로그램을 실행하십시오.
* 이용 약관에 동의하고 설치하십시오.
* 설치가 완료된 후에는 symlink를 작성해야 합니다.

## Linux 예제
{:#setup-ssl-vpn-connections-linux-example}

1. 브라우저를 열고 `http://www.softlayer.com/vpn-access`로 이동하십시오.
* 고객 포털 사용자 이름과 비밀번호로 로그인하십시오.
* 연결되면 **네트워크** 탭을 선택하십시오.
* 연결/설치 단추가 표시됩니다. 해당 단추를 선택하십시오. Java 컴포넌트를 설치하라는 프롬프트가 표시됩니다.
* 컴포넌트가 기본 위치에 설치되도록 하십시오. 기본 위치는 수동으로 작성해야 할 수 있습니다 (`/usr/local/array_vpn`).
* 설치된 후, 사용자가 연결되었음을 알리는 창이 나타납니다.
* 이 창은 VPN 터널을 이용하기 위해 계속 열려 있어야 하지만, 최소화할 수 있습니다.
* 연결을 테스트하려면 10.0.80.11 또는 서버의 사설 주소에 대해 ping을 실행하십시오. 응답을 얻으면 성공적으로 연결되었습니다.
* 완료했을 때 '네트워크' 탭 아래의 연결 끊기 단추를 선택하거나 단순히 모든 브라우저 창을 닫으십시오.

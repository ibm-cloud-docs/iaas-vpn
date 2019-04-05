---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL VPN에 연결 – MAC OSX 10x 이상
{:#connect-ssl-vpn-mac-osx}

Apple 스토어에서 최신 버전의 Mac MotionPro 클라이언트 v1.1.7을 설치하십시오. 업데이트하기 전에 이전 버전을 설치 제거하십시오.

새 클라이언트를 설치한 후 다음 디렉토리로 이동하여 터미널 애플리케이션을 사용하여 VPN을 시작하십시오. 

`/usr/local/motionpro/`

여기에서 다음 명령을 실행하여 SSL VPN에 연결하십시오.

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

[여기](https://www.softlayer.com/vpn-access)에 VPN 엔드포인트 목록이 있습니다.

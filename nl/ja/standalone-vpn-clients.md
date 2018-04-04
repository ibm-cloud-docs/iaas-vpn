---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# スタンドアロン VPN クライアント - Windows、Linux、および Mac OS X

## Windows スタンドアロン・クライアント

Windows (8/7/Vista/XP) 32 ビット:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) 64 ビット:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. ご使用のオペレーティング・システムに応じて、上記のファイルのいずれかをダウンロードします。
* MotionProSetup を実行してソフトウェアをインストールします。
* MotionPro を実行し、開始画面で**「プロファイル」->「追加」**を選択します。
* サイト名を指定し、SSL VPN サイトのリスト (下記) からホスト名を選択して、プロファイルを作成します。次に、ご使用の VPN ユーザー名とパスワードを入力し、**「保存」**をクリックします。
* 最後に、作成したプロファイルをダブルクリックして VPN に接続します。

**注**
 * 「サイト」にはドメイン・ネームまたは IP アドレスを指定できます。
 * 問題がある場合は、Windows の「コントロール パネル」を使用して Array プログラムをアンインストールし、リブートし、再接続します。
 * Windows 8 RT では機能しません。

## Linux スタンドアロン・クライアント

CentOS 64 ビット: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat 32 ビット: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat 64 ビット: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32 ビット: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64 ビット: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. `chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh` を実行可能にします。
* スクリプト `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh` を実行します。
* 使用法:  `./MotionPro --host [site] --user [username] --passwd [password]`
* 停止するには `[control-c]` を使用します。

**注:**  
 * MotionPro クライアントを始動するには、引数として少なくとも`ホスト名`と`ユーザー名`を入力する必要があります。
 * 「サイト」にはドメイン・ネームまたは IP アドレスを指定できます。

## Mac OS X 10.10 スタンドアロン・クライアント

MacOS StandAlone Array SSL VPN Motion Pro Plus クライアントのための手順:

1. 「Motion Pro Plus」クライアントを Apple ストアからインストールします。
* 「アプリケーション」フォルダーの下で Motion Pro Plus クライアントを見つけ、アプリケーションを開きます。
* 「プロファイル」をクリックし、次に「追加」をクリックします。
* 「サイト名」、「ホスト」、および「ユーザー名」に入力し、「OK」をクリックします。
* 左上にある「VPN」をクリックして接続します。

次のような画面が表示されます。

![図 1](images/snip20170425_1.png)

トンネルが正しくトラフィックを送信していなければ、[手動での経路の追加](https://discussions.apple.com/thread/2735376)が必要になる場合があります。

*更新する前に、旧バージョンをすべてアンインストールしてください。*

## SSL VPN POP (サイト)

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


**注意: 新規バージョンをインストールする前に、旧バージョンのクライアントをすべてアンインストールしてください。**

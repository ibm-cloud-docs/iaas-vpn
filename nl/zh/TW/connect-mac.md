---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 連接至 SSL VPN - MAC OSX 10x 及更高版本
{:#connect-ssl-vpn-mac-osx}

從 Apple Store 安裝最新版的 Mac MotionPro 用戶端 1.1.7 版。請務必先解除安裝所有舊版再進行更新。

安裝新用戶端之後，請移至下列目錄並使用終端機應用程式啟動 VPN。 

`/usr/local/motionpro/`

從那裡，執行下列指令以連接至 SSL VPN：

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

可以在[這裡](https://www.softlayer.com/vpn-access)找到 VPN 端點的清單。

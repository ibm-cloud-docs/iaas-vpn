---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Verbindung zu SSL-VPN herstellen - MAC OSX 10x und aktuellere Versionen
{:#connect-ssl-vpn-mac-osx}

Installieren Sie die neueste Version des Mac MotionPro-Clients v1.1.7 aus dem Apple Store. Deinstallieren Sie alle vorherigen Versionen, bevor Sie eine Aktualisierung durchführen.

Rufen Sie nach der Installation des neuen Clients das folgende Verzeichnis auf und starten Sie VPN mit der Terminalanwendung. 

`/usr/local/motionpro/`

Führen Sie dort den folgenden Befehl aus, um eine Verbindung zu SSL-VPN herzustellen:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

Eine Liste der VPN-Endpunkte finden Sie [hier](https://www.softlayer.com/vpn-access).

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eigenständige VPN-Clients - Windows, Linux und Mac OS X

## Eigenständiger Windows-Client

Windows (8/7/Vista/XP) 32-Bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) 64-Bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. Laden Sie abhängig von Ihrem Betriebssystem eine der oben aufgeführten Dateien herunter.
* Führen Sie MotionProSetup aus, um die Software zu installieren.
* Führen Sie MotionPro aus und wählen Sie in der Eingangsanzeige **Profil -> Hinzufügen** aus.
* Erstellen Sie durch Festlegen eines Sitenamens und Auswählen eines Hostnamens aus der (nachfolgenden) Liste der SSL-VPN-Sites ein Profil. Geben Sie anschließend den VPN-Benutzernamen und das zugehörige Kennwort ein und klicken Sie auf **Speichern**.
* Klicken Sie zum Schluss doppelt auf das soeben erstellte Profil, um einen Verbindung zum VPN herzustellen.

**Hinweise**
 * Eine 'Site' kann entweder ein Domänenname oder eine IP-Adresse sein.
 * Falls Probleme auftreten, deinstallieren Sie alle Array-Programme mithilfe der Windows-Systemsteuerung, führen einen Neustart durch und stellen anschließend erneut eine Verbindung her.
 * Diese Vorgehensweise kann nicht auf Windows 8 RT angewendet werden.

## Eigenständiger Linux-Client

CentOS 64-Bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Red Hat 32-Bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Red Hat 64-Bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32-Bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64-Bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. Machen Sie die Datei ausführbar: `chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* Führen Sie das Script aus: `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh.`
* Syntax: `./MotionPro --host [Site] --user [Benutzername] --passwd [Kennwort]`
* Befehl zum Stoppen: `[control-c]`

**Hinweise:**  
 * Zum Starten des MotionPro-Clients müssen Sie mindestens `hostname` und `username` als Argumente eingeben.
 * Eine 'Site' kann entweder ein Domänenname oder eine IP-Adresse sein.

## Eigenständiger Mac OS X 10.10-Client

Schritte für den eigenständigen Array-Client 'Motion Pro Plus' für SSL-VPN in Mac OS:

1. Installieren Sie den Client 'Motion Pro Plus' aus dem Apple Store.
* Suchen Sie den Client 'Motion Pro Plus' im Ordner 'Anwendungen' und öffnen Sie die Anwendung.
* Klicken Sie auf 'Profil' und anschließend auf 'Hinzufügen'.
* Geben Sie den Sitenamen, Host und Benutzernamen ein, und klicken Sie anschließend auf 'Ok'.
* Klicken Sie in der rechten oberen Ecke auf 'VPN' und stellen Sie anschließend eine Verbindung her.

Nachfolgend ein Beispiel:

![Abbildung 1](images/snip20170425_1.png)

Wenn der Datenverkehr nicht ordnungsgemäß durch den Tunnel geleitet wird, kann es erforderlich sein, die [Routen manuell hinzuzufügen](https://discussions.apple.com/thread/2735376).

*Deinstallieren Sie alle vorherigen Versionen, bevor Sie eine Aktualisierung durchführen.*.

## SSL-VPN-Bereitstellungspunkte (Sites)

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


**Hinweis: Deinstallieren Sie alle vorherigen Versionen des Clients, bevor Sie die neue Version installieren.**

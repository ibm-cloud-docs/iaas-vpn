---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL-VPN-Verbindungen konfigurieren

Für Windows, Linux Fedora und Linux sind individualisierte Verbindungsanweisungen erforderlich, die in diesem Dokument bereitgestellt werden. Nachfolgend werden einige Beispiele für die Verwendung einer SSL-VPN-Verbindung aufgeführt:

* Remote Desktop zur Back-End-IP-Adresse des Servers (10.4.X.X) zur Verwaltung der Windows 2003-Server.
* SSH zur Back-End-IP-Adresse des Servers (10.4.X.X) zur Verwaltung der UNIX-Server.
* Verwendung eines IPMI-Clients zum Steuern des Servers mithilfe der Back-End-IPMI-Adresse (10.4.X.X). Sie können das IPMI-Client-Tool durch Aufrufen von http://downloads.service.softlayer.com herunterladen.
  * **Hinweis:** Für IPMIView muss Java installiert sein; Sie können Java unter http://www.sun.com/java/ herunterladen.
* Testen der Website an den Back-End-IP-Adressen, bevor sie an den öffentlich zugänglichen IP-Adressen aktiviert werden.
* Dateiübertragung der sicheren Daten zwischen dem/den Server(n) und dem Heimarbeitsplatz/Büro.
* Sicherung der Konfigurationsdateien für den/die Server im Heimarbeitsplatz/Büro.
* Sichere Verbindung zum Webportal unter http://manage.service.softlayer.com.

## Windows (Internet Explorer)

1. Öffnen Sie Internet Explorer und navigieren Sie zu http://www.softlayer.com/vpn-access.
* Sobald Sie Ihren Benutzernamen und Ihr Kennwort eingegeben haben, werden Sie aufgefordert, ein ActiveX-Plug-in zu installieren. Sie müssen dieses Plug-in installieren, damit Sie eine Verbindung zum Back-End-Netz herstellen können. 
* Sie müssen auf der Workstation auch über Administratorberechtigungen verfügen, um das ActiveX-Plug-in installieren zu können. Falls Sie nicht über diese Berechtigungen verfügen, fragen Sie Ihren lokalen Systemadministrator, damit er es für Sie installiert. 
* Sobald das ActiveX-Plug-in installiert ist, wird ein Array-Netzkonnektor für SSL-VPN gestartet und stellt eine Verbindung zum VPN-Gerät her. Wenn der Verbindungsaufbau erfolgreich ist, wird in der Taskleiste ein rotes '**A**' angezeigt. Sie können jederzeit auf das '**A**' klicken, um den Status der SSL-VPN-Verbindung anzuzeigen: den Status, die zugewiesene IP-Adresse, die zugewiesenen DNS-Server, die Netzrouten und die verbundene Zeit. 
* Sie können die Browsersitzung jederzeit minimieren und andere Anwendungen sicher im privaten Netz verwenden. 
* Wenn Sie fertig sind, trennen Sie die Verbindung durch Auswählen der Schaltfläche für die Trennung auf der rechten Seite oder einfach durch Schließen des Fensters.

## Linux Fedora (FireFox)

Es wird empfohlen, alle Befehle als Root auszuführen. (`setuid root`)

1. Laden Sie Java von `http://java.com/en/download/manual.jsp` herunter. Hierbei handelt es sich um eine selbstextrahierende Linux-Datei.
* Schließen Sie FireFox.
* Verschieben Sie die Datei an die Position, an der Sie Java installieren möchten (in der Regel `/usr/local`).
* Machen Sie die Datei mithilfe des Befehls `chmod +x jre-6u1-linux-i586.bin` ausführbar.
* Führen Sie das Installationsprogramm mithilfe des Befehls `./jre-6u1-linux-i586.bin` aus.
* Akzeptieren Sie die Nutzungsbedingungen und führen Sie die Installation durch.
* Sobald die Installation abgeschlossen ist, müssen Sie eine symbolische Verbindung erstellen.

## Linux-Beispiel
```
cd /usr/lib/firefox-1.0.4/plugins/
ln -s /usr/local/jre-6u1/plugin/i386/ns7/libjavaplugin_oji.so .
```

1. Öffnen Sie Firefox und rufen Sie `http://www.softlayer.com/vpn-access` auf.
* Melden Sie sich mit dem Benutzernamen und Kennwort des Kundenportals an.
* Wählen Sie die Registerkarte **Netz** aus, sobald die Verbindung hergestellt ist.
* Eine Schaltfläche zum Herstellen einer Verbindung bzw. Installieren sollte angezeigt werden. Wählen Sie sie aus; daraufhin werden Sie aufgefordert, die Java-Komponente zu installieren.
* Führen Sie die Installation der Komponente im Standardpfad durch, den Sie unter Umständen manuell erstellen müssen. (`/usr/local/array_vpn`)
* Wenn die Installation abgeschlossen ist, wird ein Fenster angezeigt, das besagt, dass eine Verbindung hergestellt wurde.
* Dieses Fenster muss geöffnet bleiben, damit der VPN-Tunnel verwendet werden kann; Sie können es aber minimieren.
* Setzen Sie zum Testen der Verbindung ein Pingsignal an 10.0.80.11 oder an die private Adresse des Servers ab. Wenn Sie eine Antwort erhalten, wurde die Verbindung erfolgreich hergestellt.
* Wenn Sie fertig sind, wählen Sie die Schaltfläche zum Trennen der Verbindung in der Registerkarte für das Netz aus oder schließen einfach alle Browserfenster.

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL-VPN verwenden

1. Navigieren Sie zum Link **SSL-VPN-Anmeldung** im Kundenportal; wählen Sie hierzu **Support > SSL-VPN-Anmeldung** im Navigationsmenü aus und geben Sie anschließend Ihre Berechtigungsnachweise ein.
2. Der SSL-VPN-Tunnel ist aufgebaut, wenn der Buchstabe 'A' in der Taskleiste angezeigt wird.
3. Herzlichen Glückwunsch - Sie sind jetzt mit Ihrem privaten VLAN verbunden.

## Was soll ich nach der Herstellung meiner Verbindung tun?

1. Verwenden Sie SSH oder RDC (Terminalservices) zum Herstellen der Verbindung zur privaten IP-Adresse des Servers (10.x.x.x) zur Serververwaltung.
2. Wenn Sie Funktionen der fernen Konsole oder Warmstartfunktionen verwenden möchten, stellen Sie eine Verbindung zur IPMI 2.0-Karte über die SuperMicro-Software her; Informationen zum Herunterladen finden Sie im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
3. Sie können dem Server (Windows) ein Laufwerk zuordnen oder ein Laufwerk an den Server anhängen (Red Hat).

## Tipps und Tricks

1. Die IPMI-IP und die private IP ähneln sich sehr, sind aber unterschiedlich - verwechseln Sie sie nicht.
2. Sie können nicht SSH oder RDC für den Verbindungsaufbau zur IPMI-Karte verwenden; hierfür müssen Sie die Software verwenden.
3. Die IPMI-IP und die private IP finden Sie im Hardwareabschnitt unter jedem **Server**.
4. Die IPMI-Karte ist an der privaten IP-Schnittstelle 'empfangsbereit' und leitet den IPMI-Datenverkehr an die IPMI-Karte zurück.

**Warnung:**

Wenn Sie `eth0` inaktivieren (die private Netzschnittstelle), steht die gesamte IPMI-Funktionalität einschließlich Überwachung, ferner Konsole, fernem Warmstart, usw. nicht mehr zur Verfügung. Wenn Sie den Zugriff auf die private Schnittstelle sperren möchten, finden Sie Informationen hierzu in der Liste der zulässigen IP-Adressen, die Sie in die IP-Tabellen oder Server-Firewalls eingeben können.

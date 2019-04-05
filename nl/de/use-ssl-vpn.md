---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# SSL-VPN verwenden
{:#use-ssl-vpn}

1. Navigieren Sie zum Link **SSL-VPN-Anmeldung** im Kundenportal; wählen Sie hierzu **Support > SSL-VPN-Anmeldung** im Navigationsmenü aus und geben Sie anschließend Ihre Berechtigungsnachweise ein.
2. Der SSL-VPN-Tunnel ist aufgebaut, wenn der Buchstabe 'A' in der Taskleiste angezeigt wird.
3. Herzlichen Glückwunsch - Sie sind jetzt mit Ihrem privaten VLAN verbunden.

## Was soll ich nach der Herstellung meiner Verbindung tun?
{:#now-im-connected-what-do-i-do}

1. Verwenden Sie SSH oder RDC (Terminalservices) zum Herstellen der Verbindung zur privaten IP-Adresse des Servers (10.x.x.x) zur Serververwaltung.
2. Wenn Sie Funktionen der fernen Konsole oder Warmstartfunktionen verwenden möchten, stellen Sie eine Verbindung zur IPMI 2.0-Karte über die SuperMicro-Software her; Informationen zum Herunterladen finden Sie im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/).
3. Sie können dem Server (Windows) ein Laufwerk zuordnen oder ein Laufwerk an den Server anhängen (Red Hat).

## Tipps und Tricks
{:#ssl-vpn-tips-tricks}

1. Die IPMI-IP und die private IP ähneln sich sehr, sind aber unterschiedlich - verwechseln Sie sie nicht.
2. Sie können nicht SSH oder RDC für den Verbindungsaufbau zur IPMI-Karte verwenden; hierfür müssen Sie die Software verwenden.
3. Die IPMI-IP und die private IP finden Sie im Hardwareabschnitt unter jedem **Server**.
4. Die IPMI-Karte ist an der privaten IP-Schnittstelle 'empfangsbereit' und leitet den IPMI-Datenverkehr an die IPMI-Karte zurück.

## Produktspezifische IPMI-Anweisungen
{:#product-specific-impi-instructions}

* Weitere Informationen zur Verwendung von IPMI in einer CIFS-Freigabe finden Sie unter [ISO an einen Bare-Metal-Server anhängen](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-).
* Weitere Informationen zur Verwendung von IPMI mit VMWare finden Sie unter [VMware vSphere ESXi über ferne Konsole und virtuelle Medien installieren](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi).

* Weitere Informationen zur Verwendung von IPMI mit IBM POWER-Hardware finden Sie unter [IPMItool installieren](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm).

**Warnung:**

Wenn Sie `eth0` inaktivieren (die private Netzschnittstelle), steht die gesamte IPMI-Funktionalität einschließlich Überwachung, ferner Konsole, fernem Warmstart, usw. nicht mehr zur Verfügung. Wenn Sie den Zugriff auf die private Schnittstelle sperren möchten, finden Sie Informationen hierzu in der Liste der zulässigen IP-Adressen, die Sie in die IP-Tabellen oder Server-Firewalls eingeben können.

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Einstellung der Unterstützung für PPTP-VPN
{:#pptp-vpn-deprecation}

PPTP-VPN wird seit 12. Juni 2018 nicht mehr unterstützt und wird Kunden nicht mehr angeboten. Vielen Dank für Ihr Interesse. Informationen zu möglichen Alternativen finden Sie in den folgenden Abschnitten.

## Was ist VPN?
{:#pptp-vpn-deprecation-what-is-vpn}
VPN-Zugriff ermöglicht den Benutzern, alle Server remote und sicher über das private Netz einer IBM Cloud zu verwalten. Die VPN-Verbindung von Ihrem Standort zum privaten Netz ermöglicht Out-of-band-Management und Serverrettung über einen verschlüsselten VPN-Tunnel. Mit VPN-Zugriff verfügen Sie über folgende Möglichkeiten:

* Aufbau einer VPN-Verbindung zu einem privaten Netz über SSL, **PPTP** oder IPSec
* Zugriff auf den Server über die private 10.x.x.x-IP-Adresse über SSH oder RDP
* Verbindung zur IPMI-IP-Adresse des Servers zur zusätzlichen Serververwaltung oder zu Rettungszwecken

## Einstellung der Unterstützung für PPTP
{:#pptp-deprecation-vpn}
Da andere VPN-Optionen immer sicherer und vielseitiger werden, wird der Bedarf für PPTP geringer. {{site.data.keyword.BluSoftlayer_notm}} bietet eine Reihe anderer Optionen, wie z. B. SSL oder IPSec, die weiter entwickelt und sicherer sind als PPTP.

**Daher bietet {{site.data.keyword.BluSoftlayer_notm}} PPTP seit 12. Juni 2018 nicht mehr an.**
{:important}


## Häufig gestellte Fragen
{:#pptp-vpn-deprecation-faq}

**F: Warum wurde die Unterstützung für PPTP eingestellt?**

**A:** Um auch weiterhin Schutzfunktionen der höchsten Qualität bereitzustellen, hat {{site.data.keyword.BluSoftlayer_notm}} entschieden, die Verwendung und Unterstützung von PPTP einzustellen. {{site.data.keyword.BluSoftlayer_notm}} möchte das Versprechen an die Kunden aufrecht erhalten, dass die Sicherheit ihrer Daten und personenbezogenen Informationen von größter Bedeutung ist. 

**F: Welche anderen VPN-Zugriffstypen außer PPTP sind verfügbar?**

**A:** {{site.data.keyword.BluSoftlayer_notm}} bietet eine Reihe von Optionen an, für die eine einfache Konfiguration genügt.
  1. SSL-VPN ist eine Schnellzugriffsverbindung, die direkt vom eigenen Browser zum privaten Netz hergestellt wird. Eine SSL-VPN-Verbindung ist mit Windows XP und aktuelleren Windows-Versionen sowie ActiveX, Fedora, Ubuntu und Mac OSX kompatibel. Der globale Zugriff auf das private Netz ist über eine einzige URL verfügbar, was die Auswahl des nächstmöglichen VPN-Endpunkts ermöglicht. In [SSL-VPN-Verbindung einrichten](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) finden Sie weitere Details zur Einführung in diese Option.
  2. IPsec ist eine Protokollgruppe zur Authentifizierung und Verschlüsselung des gesamten IP-Datenverkehrs zwischen zwei Standorten. Es ermöglicht das Übertragen vertrauenswürdiger Daten über Netze, die sonst als nicht sicher angesehen würden. Weitere allgemeine Informationen zu IPSec sowie Informationen zum Einstieg in die Verwendung dieses Service finden Sie in [IPSec-VPN einrichten](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) und in den anderen [Referenzdokumenten](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation). 

**F: Wie gehe ich vor, wenn für meine geschäftsrelevanten Prozesse und Verfahren PPTP erforderlich ist?**

**A:** Falls Sie PPTP für Ihre Geschäftsanforderungen benötigen, stehen Ihnen eine Reihe von Optionen zur Verfügung. **Nicht alle möglichen Optionen sind hier aufgeführt. Beachten Sie, dass für die folgenden Optionen eine vollständige Konfiguration beider Endpunkte erforderlich ist. Für die Konfiguration dieser Optionen ist der Kunde verantwortlich.**
  1. Virtual Router Appliance. Virtual Router Appliance, auch bekannt als Vyatta, dient als Gateway und Router für Ihre Umgebung. Dieses Produkt umfasst Zonen, die Teilnetze enthalten. Firewallregeln werden zwischen den Zonen eingerichtet und steuern die Kommunikation zwischen diesen. Für Zonen, die nicht mit anderen Zonen kommunizieren müssen, ist keine Firewallregel erforderlich, da alle Pakete gelöscht werden. [Einführung in Virtual Router Appliance](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance) enthält weitere Details zum Einstieg in diesen Service. 
  2. FSA-Firewall. FortiGate Security Appliance (FSA) 10 Gb/s ist eine Hardware-Firewall, die zum Schutz des Datenverkehrs in mehreren VLANs sowohl für öffentliche als auch für private Netze konfiguriert werden kann. Im Kundenportal wird sie als “Firewall für mehrere VLANs” bezeichnet. [Einführung in FSA 10 Gb/s](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) enthält weitere Details zum Einstieg in diesen Service. 
 
Die oben beschriebenen Optionen stellen einige der Möglichkeiten dar, die Sie testen können, nachdem der Service von {{site.data.keyword.BluSoftlayer_notm}} nicht mehr bereitgestellt wird, falls PPTP für Ihre Geschäftsanforderungen erforderlich ist. Danke für die Zusammenarbeit.
{:note}

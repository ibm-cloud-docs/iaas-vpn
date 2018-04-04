---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informationen zu VPN

VPN-Zugriff ermöglicht Ihnen die Verwaltung aller Server und Services, die Ihrem Konto zugeordnet sind, remote über das private Netz einer IBM Cloud. Die VPN-Verbindung von Ihrem Standort zum privaten Netz ermöglicht Out-of-band-Management und Serverrettung über einen verschlüsselten VPN-Tunnel.

Die Kommunikation mithilfe eines privaten Netzes ist naturgemäß sicherer. So haben Sie die Möglichkeit, öffentlichen Zugriff zu begrenzen und gleichzeitig ihre Server zu verwalten. Jedem Benutzer kann für sein eigenes Konto VPN-Zugriff gewährt werden; verfügbar sind SSL und PPTP. Mithilfe von VPN-Interaktionen auf dem [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) kann der VPN-Zugriff auf Benutzerebene angepasst werden.

## Welche Möglichkeiten gibt es zur Verwendung von SSL-VPN?

Über dieses sichere Out-of-band-Gateway können Sie über das private Netz auf den Server zugreifen. Gängige Varianten sind hierbei:

* Verbindung zur privaten IP-Adresse des Servers (10.x.x.x) für SSH oder RDC.
* Verbindung zur IPMI-Karte für die ferne Konsole/fernen Zugriff/ferne Überwachung.
* Anhängen von Laufwerken in Windows oder Red Hat des Home Office- oder Arbeits-PCs zur Erleichterung der Arbeit.
* Beenden einer allgemein zugänglichen Schnittstelle auf Datenbankservern und Verwaltung über das private Netz.
* Beenden einer allgemein zugänglichen Schnittstelle während der Erstkonfiguration des Servers.
* Beenden einer allgemein zugänglichen Schnittstelle während Sicherheitsupdates.
* Beenden einer allgemein zugänglichen Schnittstelle während einer Sicherheitsverletzung und Behebung des Problems über das private Netz.

## Hauptmerkmale

 * Mit dem privaten Netz ist eine kostenlose Kommunikation zu den Servern und Verwaltung der Server möglich. Das VPN ist das Gateway zu diesem privaten Netz.
 * Als Optionen stehen SSL-VPN und PPTP-VPN zur Verfügung.
 * Die weltweiten Zugangspunkte bieten schnellste Zugriffe und Interaktionen. IBM Cloud verfügt derzeit über VPN-Zugriffspunkte in vielen Städten.
 * Eine Liste der VPN-Zugriffspunkte zum privaten Netz von {{site.data.keyword.BluSoftlayer_notm}} finden Sie unter http://www.softlayer.com/vpn-access.

## Funktionsweise

Für VPN-Zugriff gibt es zwei Möglichkeiten für die Verbindung zum privaten Netz und Verwalten der Server und Services. Diese Optionen sind die VPN-Verbindungen über SSL und PPTP. Stellen Sie Ihre Verbindung abhängig von Ihren jeweiligen Anforderungen oder Vorgaben mithilfe einer dieser beiden Methoden her.
 
## SSL-VPN-Verbindungen

SSL-VPN ist eine Schnellzugriffsverbindung, die direkt vom eigenen Browser zum privaten Netz hergestellt wird. Eine SSL-VPN-Verbindung ist mit Windows XP und aktuelleren Windows-Versionen sowie ActiveX, Fedora, Ubuntu und Mac OSX kompatibel. Der globale Zugriff auf das private Netz ist über eine einzige URL verfügbar, was die Auswahl des nächstmöglichen VPN-Endpunkts ermöglicht.

## SSL-VPN-Teilnetzbegrenzung

Der SSL-VPN-Client weist ein festes 64-Teilnetzlimit auf, das er zum Füllen seiner Routing-Tabelle verwenden kann. Wenn ein Konto aus über 64 Teilnetzen besteht, stellen Sie sicher, dass Sie Ihre SSL-VPN-Berechtigungen so ändern, dass eine manuelle Teilnetzzuweisung verwendet wird. Falls Sie dies nicht tun, können manche Teilnetze unter Umständen nicht mehr über das SSL-VPN erreichbar sein.

## PPTP-VPN-Verbindungen

Über PPTP-VPN-Verbindungen können Sie eine Verbindung zu einem privaten Netz sicher über betriebssystemspezifische Client-Software vom Desktop oder unter Verwendung einer dedizierten Einheit wie einer Firewall oder eines Routers herstellen. Eine VPN-Konnektivität wird derzeit für Windows XP und aktuelleren Windows-Versionen sowie Fedora, Ubuntu und Mac OSX bereitgestellt. Die PPTP-Verbindungsoption ist für die Verbindung eines gesamten Büros konzipiert oder für Fälle, in denen eine Verbindung über SSL-VPN nicht möglich ist. PPTP-Verbindungen werden mit einem einzigen Rechenzentrum hergestellt, das beim Einrichten der VPN-Verbindung ausgewählt werden kann.

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# Häufig gestellte Fragen zu VPN
{:#vpn-faq}

## Was ist IBM Cloud-VPN?
{:#what-is-ibm-cloud-vpn}
{:faq}

IBM Cloud-VPN soll den Benutzern die ferne und sichere Verwaltung aller Server über das private Netz in der IBM Cloud ermöglichen.  Die VPN-Verbindung von Ihrem Standort zum privaten Netz ermöglicht Out-of-band-Management und Serverrettung über einen verschlüsselten VPN-Tunnel. Mit VPN-Zugriff verfügen Sie über folgende Möglichkeiten:

* Aufbau einer VPN-Verbindung zu einem privaten Netz mithilfe von SSL oder IPsec
* Zugriff auf den Server über die private 10.x.x.x-IP-Adresse mithilfe von SSH oder RDP
* Verbindung zur IPMI-IP-Adresse des Servers zur zusätzlichen Serververwaltung oder zu Rettungszwecken


## Können für SSL-VPN auch die Protokolle PPTP, IPsec oder andere VPN-Protokolle verwendet werden?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Derzeit wird vom SSL-VPN-Gateway ein browserbasiertes SSL-VPN-Plug-in oder ein proprietärer Client zum Aufbauen der Verbindungen verwendet. An weiteren Optionen für die VPN-Konnektivität zum privaten Netzwerk wird gearbeitet. Das SSL-VPN wurde aufgrund seiner Benutzerfreundlichkeit und Kompatibilität ausgewählt. PPTP wird nicht weiter unterstützt. Weitere Informationen finden Sie unter [Einstellung der Unterstützung für PPTP-VPN](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).



## Kann ich den NAS/FTP-Server von meinem fernen Standort über das SSL-VPN-Gateway anhängen?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

Nein. Sie haben nur Zugriff auf das private VLAN und die Server vom SSL-VPN-Gateway. Wenn Sie Daten von Ihrem NAS/FTP-Datenträger herunterladen möchten, müssen Sie die Daten auf den Server und anschließend über das VPN zum fernen Standort verschieben.

Aus Sicherheitsgründen verfügen nur Server im Rechenzentrum über Zugriff auf Server, von denen Services bereitgestellt werden (DNS, Update, NAS, Lockbox).


## Welcher Anbieter stellt SSL-VPN bereit und wie funktioniert es?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Das SSL-VPN-Gateway ist ein Sicherheitsprodukt von Array Networks.  Auf dem Gateway selbst wird Radius zum Aktualisieren der Benutzer und Kennwörter des Kundenportals ausgeführt. Wenn Sie Benutzer hinzufügen möchten und Ihnen SSL-VPN-Zugriff gewähren möchten, erstellen Sie einen neuen Benutzer im Kundenportal und aktivieren die SSL-VPN-Berechtigungen.


## Was ist der Unterschied zwischen SSL- und PPTP-VPN?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

**SSL-VPN** ermöglicht einem Benutzer die Erstellung eines sicheren Tunnels von einem fernen Desktop zum privaten {{site.data.keyword.BluSoftlayer_notm}}-Netz. Dieses VPN ist mit einer Vielzahl an Betriebssystemen kompatibel.

**PPTP-VPN** ermöglicht denselben sicheren Tunnel, stellt die Verbindung aber über eine besondere Client-Software auf dem Benutzerdesktop oder einer dedizierten Einheit her. PPTP wird jedoch nicht weiter unterstützt. Weitere Informationen finden Sie unter [Einstellung der Unterstützung für PPTP-VPN](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Warum kann ich keine weiteren Benutzer zum PPTP-VPN hinzufügen?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP wird nicht weiter unterstützt. Weitere Informationen finden Sie unter [Einstellung der Unterstützung für PPTP-VPN](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Welche Kategorien für den Status eines Benutzers für die VPN-Verwaltung sind im Kundenportal verfügbar?
{:#what-are-available-categories-vpn-management}
{:faq}

Die Kundenstatuskategorien umfassen Kategorien, die vom Benutzer aktualisiert werden können, und Kategorien, die automatisch angezeigt werden können. Dabei handelt es sich um folgende Kategorien:

* **Aktiv** - Der Benutzer verfügt über Zugriff auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) und das VPN basiert auf den Berechtigungen, die vom Kontoadministrator festgelegt wurden. Dieser Status kann jederzeit manuell ausgewählt oder geändert werden.
* **Inaktiviert** - Der Benutzer verfügt nicht über Zugriff auf Berechtigungen oder Abonnements für das Konto, auch nicht auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) und das VPN. Wenn dieser Status von einem anderen Benutzer des Kontos auf 'Inaktiviert' gesetzt wurde, kann er jederzeit manuell ausgewählt und geändert werden.
* **Nur VPN** - Der Benutzer verfügt nur über Zugriff auf die VPN-Konnektivität und kann nicht auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) zugreifen. Dieser Status kann jederzeit manuell ausgewählt oder geändert werden.
* **Inaktiv** - Der Benutzer hat das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) oder VPN in den letzten 60 Tagen nicht verwendet. Hierbei handelt es sich um einen vom System generierten Status.
* **Stornierung anstehend** - Ein Administrator für das Konto hat diesen Benutzer storniert und die Stornierung wird derzeit verarbeitet. Hierbei handelt es sich um einen vom System generierten Status.

## Wie wird SSL-VPN eingerichtet?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

Ausführliche Anweisungen finden Sie unter [Verbindung zu SSL-VPN herstellen - Windows 7 und aktuellere Versionen](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



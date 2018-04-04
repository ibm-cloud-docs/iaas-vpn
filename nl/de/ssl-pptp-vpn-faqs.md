---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Häufig gestellte Fragen zu VPN

## Was ist IBM Cloud-VPN?

IBM Cloud-VPN soll den Benutzern die ferne und sichere Verwaltung aller Server über das private Netz in der IBM Cloud ermöglichen. Die VPN-Verbindung von Ihrem Standort zum privaten Netz ermöglicht Out-of-band-Management und Serverrettung über einen verschlüsselten VPN-Tunnel. Mit VPN-Zugriff verfügen Sie über folgende Möglichkeiten:

* Aufbau einer VPN-Verbindung zu einem privaten Netz mithilfe von SSL, PPTP oder IPsec
* Zugriff auf den Server über die private 10.x.x.x-IP-Adresse mithilfe von SSH oder RDP
* Verbindung zur IPMI-IP-Adresse des Servers zur zusätzlichen Serververwaltung oder zu Rettungszwecken


## Können für SSL-VPN auch die Protokolle PPTP, IPsec oder andere VPN-Protokolle verwendet werden?

Derzeit wird vom SSL-VPN-Gateway ein browserbasiertes SSL-VPN-Plug-in oder ein proprietärer Client zum Aufbauen der Verbindungen verwendet. An weiteren Optionen für die VPN-Konnektivität zum privaten Netzwerk wird gearbeitet. Das SSL-VPN wurde aufgrund seiner Benutzerfreundlichkeit und Kompatibilität ausgewählt.


<a name="152"></a>
## Kann ich den NAS/FTP-Server von meinem fernen Standort über das SSL-VPN-Gateway anhängen?

Nein. Sie haben nur Zugriff auf das private VLAN und die Server vom SSL-VPN-Gateway. Wenn Sie Daten von Ihrem NAS/FTP-Datenträger herunterladen möchten, müssen Sie die Daten auf den Server und anschließend über das VPN zum fernen Standort verschieben.

Aus Sicherheitsgründen verfügen nur Server im Rechenzentrum über Zugriff auf Server, von denen Services bereitgestellt werden (DNS, Update, NAS, Lockbox).

<a name="175"></a>
## Welcher Anbieter stellt SSL-VPN bereit und wie funktioniert es?

Das SSL-VPN-Gateway ist ein Sicherheitsprodukt von Array Networks.  Auf dem Gateway selbst wird Radius zum Aktualisieren der Benutzer und Kennwörter des Kundenportals ausgeführt. Wenn Sie Benutzer hinzufügen möchten und Ihnen SSL-VPN-Zugriff gewähren möchten, erstellen Sie einen neuen Benutzer im Kundenportal und aktivieren die SSL-VPN-Berechtigungen.

<a name="276"></a>
## Was ist der Unterschied zwischen SSL- und PPTP-VPN?

**SSL-VPN** ermöglicht einem Benutzer die Erstellung eines sicheren Tunnels von einem fernen Desktop zum privaten {{site.data.keyword.BluSoftlayer_notm}}-Netz. Dieses VPN ist mit einer Vielzahl an Betriebssystemen kompatibel.

**PPTP-VPN** ermöglicht denselben sicheren Tunnel, stellt die Verbindung aber über eine besondere Client-Software auf dem Benutzerdesktop oder einer dedizierten Einheit her. PPTP-VPN eignet sich sehr gut für Benutzer, die keine SSL-Verbindung verwenden können.

## Wenn ich eine Verbindung zum PPTP-VPN herstelle, wird die Nachricht angezeigt, dass der Zugriff aufgrund eines ungültigen Benutzernamens und/oder Kennworts verweigert wird (Error 691: Access was denied because the username and/or password is invalid). Wie kann ich dieses Problem lösen?

Alle Benutzer können eine Verbindung zum PPTP-VPN herstellen, sie müssen aber über die Berechtigung zum Anmelden über das Kundenportal verfügen. PPTP-VPN-Berechtigungen werden ohne großen Aufwand überprüft und häufig aktualisiert. Weitere Informationen dazu finden Sie unter [PPTP-VPN-Zugriff aktivieren oder inaktivieren ](activate-a-user.html).

## Warum kann ich keine weiteren Benutzer zum PPTP-VPN hinzufügen?

PPTP-VPN ist zwar für alle Konten verfügbar, anfangs aber für die Aktivierung des Zugriffs für einen Benutzer gleichzeitig konfiguriert. Wenn Sie anfordern möchten, dass ein Konto für unbegrenztes PPTP ohne Aufpreis aktiviert wird, erstellen Sie ein Ticket über das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) mit den folgenden Informationen und allen weiteren Details, die unter Umständen erforderlich sind:

* Thema: PPTP-VPN-Anforderung
* Text: Ich verfüge derzeit über PPTP für einen einzigen Benutzer. Aktivieren Sie bitte den uneingeschränkten PPTP-VPN-Zugriff für mein Konto.

Ein Mitglied des IBM Support Teams aktiviert den uneingeschränkte PPTP-Zugriff für das Konto ohne Aufpreis. Das Ticket wird aktualisiert, falls weitere Informationen erforderlich sind.

## Welche Kategorien für den Status eines Benutzers für die VPN-Verwaltung sind im Kundenportal verfügbar?

Die Kundenstatuskategorien umfassen Kategorien, die vom Benutzer aktualisiert werden können, und Kategorien, die automatisch angezeigt werden können. Dabei handelt es sich um folgende Kategorien:

* **Aktiv** - Der Benutzer verfügt über Zugriff auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) und das VPN basiert auf den Berechtigungen, die vom Kontoadministrator festgelegt wurden. Dieser Status kann jederzeit manuell ausgewählt oder geändert werden.
* **Inaktiviert** - Der Benutzer verfügt nicht über Zugriff auf Berechtigungen oder Abonnements für das Konto, auch nicht auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) und das VPN. Wenn dieser Status von einem anderen Benutzer des Kontos auf 'Inaktiviert' gesetzt wurde, kann er jederzeit manuell ausgewählt und geändert werden.
* **Nur VPN** - Der Benutzer verfügt nur über Zugriff auf die VPN-Konnektivität und kann nicht auf das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) zugreifen. Dieser Status kann jederzeit manuell ausgewählt oder geändert werden.
* **Inaktiv** - Der Benutzer hat das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) oder VPN in den letzten 60 Tagen nicht verwendet. Hierbei handelt es sich um einen vom System generierten Status.
* **Stornierung anstehend** - Ein Administrator für das Konto hat diesen Benutzer storniert und die Stornierung wird derzeit verarbeitet. Hierbei handelt es sich um einen vom System generierten Status.

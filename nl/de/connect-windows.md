---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Zu SSL-VPN verbinden - Windows 7 und aktuellere Versionen

Für die Verbindung zum {{site.data.keyword.BluSoftlayer_notm}}-SSL-VPN sind unter Umständen einige Schritte auf dem Computer erforderlich, um die Verbindungsfähigkeit sicherzustellen.

**1. Inaktivieren Sie in der Systemsteuerung die Benutzerkontosteuerung.**

1. Navigieren Sie zu **Start -> Systemsteuerung -> Benutzerkonten -> Einstellungen der Benutzerkontosteuerung ändern**.
* **Inaktivieren** Sie das Kästchen neben **Benutzerkontensteuerung verwenden, um zum Schutz des Computers beizutragen**.

**2. Aktivieren Sie das Administratorkonto**.

1. Wechseln Sie zu **Start -> Systemsteuerung -> Verwaltung -> Computerverwaltung -> Lokale Benutzer und Gruppen -> Benutzer ->**. 
* Klicken Sie mit der rechten Maustaste auf den Benutzer **Administrator** und wählen Sie **Eigenschaften** aus. 
* Nehmen Sie die Auswahl des Kästchens für **Konto ist deaktiviert** zurück.

**3. Führen Sie Internet Explorer als Administrator aus, bevor Sie eine Verbindung zur SSL-VPN-Seite herstellen.**

1. Klicken Sie mit der rechten Maustaste auf das Internet Explorer-Symbol und wählen Sie im Menü **Als Administrator ausführen** aus.

Sobald die obigen Schritte ausgeführt sind, muss die Anmeldung möglich sein. 

## Anmeldung

1. Rufen Sie [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) auf und melden Sie sich mithilfe Ihres Benutzernamens und Kennworts für das Portal an. 
* Stellen Sie sicher, dass der Benutzer [über SSL-VPN-Zugriff verfügt](edit-users-vpn-access.html).  
* Stellen Sie auch sicher, dass Sie ein VPN-Kennwort festgelegt haben. Aktualisieren Sie  hierzu die [Benutzerprofilseite](https://control.softlayer.com/account/user/profile) und füllen Sie das Kästchen für das **VPN-Kennwort** aus.

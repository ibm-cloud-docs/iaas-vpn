---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# PPTP-VPN für Mac OS X 10.X konfigurieren

Mit PPTP-VPN-Verbindungen kann von einem Desktop oder einer dedizierten Einheit eine Fernverbindung zu einem privaten {{site.data.keyword.BluSoftlayer_notm}}-Netz hergestellt werden. Die Herstellung der Verbindung zu einem privaten Netz über PPTP steht für eine Vielzahl an Betriebssystemen zur Verfügung, auch für Mac OS X. Die Benutzer können durch Eingeben der eindeutigen Zieladresse beim Konfigurieren eine Verbindung zu einem beliebigen {{site.data.keyword.BluSoftlayer_notm}}-Rechenzentrum herstellen. Führen Sie die folgenden Schritte aus, um eine PPTP-VPN-Verbindung in Mac OS X aufzubauen.

## PPTP-VPN-Verbindung konfigurieren

* Wählen Sie **Systemvorgaben** im Dropdown-Menü von **Apple** aus.
* Klicken Sie auf das Symbol **Netzwerk** im Abschnitt 'Internet&Netzwerk'.
* Klicken Sie auf das Symbol **Pluszeichen** ganz unten im Menü **Verbindungen**. Ein Popup-Fenster wird angezeigt, in dem Sie die VPN-Verbindung erstellen können.
* Erstellen Sie die VPN-Verbindung.
  * Wählen Sie **VPN** in der Dropdown-Liste **Schnittstelle** aus.
  * Wählen Sie **PPTP** in der Dropdown-Liste **VPN-Typ** aus.
  * Geben Sie einen **beschreibenden Titel** für die Verbindung in das Feld **Servicename** ein.
  * **Hinweis:** Es wird empfohlen, den Standort des Rechenzentrums als Bestandteil des Servicenamens zu verwenden.
  * Klicken Sie auf die Schaltfläche **Erstellen**.
* Klicken Sie im Menü 'Verbindungen' auf die soeben erstellte Verbindung.
* Geben Sie die **Zieladresse** des gewünschten Rechnungszentrums in das Feld **Serveradresse** ein. Die passende Adresse für die aktuellen {{site.data.keyword.BluSoftlayer_notm}}-Rechenzentren finden Sie in der folgenden Tabelle.
* Geben Sie den **Benutzernamen des Kundenportals** in das Feld **Kontoname** ein.
* Nehmen Sie die Einstellungen für die Authentifizierung vor.
  * Klicken Sie auf die Schaltfläche **Authentifizierungseinstellungen**. Es wird ein Popup-Fenster angezeigt, in dem Sie zum Authentifizieren des VPNs aufgefordert werden.
  * Geben Sie Ihr **VPN-Kundenkennwort** in das Feld **Kennwort** ein.
  * Klicken Sie auf die Schaltfläche **OK**.
* Aktualisieren Sie die Einstellungen für den VPN-Datenverkehr.
  * Klicken Sie auf die Schaltfläche **Erweitert**.
  * Stellen Sie sicher, dass das Kontrollkästchen **Gesamten Datenverkehr über VPN-Verbindung senden** im Abschnitt 'Sitzung' nicht ausgewählt ist.
  * Klicken Sie auf die Schaltfläche **OK**.
* Wählen Sie das Kontrollkästchen **VPN-Status in Menüleiste anzeigen** aus.
* Klicken Sie auf die Schaltfläche 'Anwenden'. Die VPN-Verbindung kann jetzt jederzeit über den VPN-Menüleistenpunkt aufgebaut werden.

|Standort des Rechenzentrums|Internetadresse des Rechenzentrums|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapore, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, HK|pptpvpn.hkg02.softlayer.com|
|Melbourne, AU|pptpvpn.mel01.softlayer.com|
|London, GB|pptpvpn.lon02.softlayer.com|
|Paris, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokyo, JP|pptpvpn.tok02.softlayer.com|

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# PPTP-VPN für Windows 7 konfigurieren

Mit PPTP-VPN-Verbindungen kann von einem Desktop oder einer dedizierten Einheit eine Fernverbindung zu einem privaten {{site.data.keyword.BluSoftlayer_notm}}-Netz hergestellt werden. Die Herstellung der Verbindung zu einem privaten Netz über PPTP steht für eine Vielzahl an Betriebssystemen zur Verfügung, auch für Windows 7. Die Benutzer können durch Eingeben der eindeutigen Zieladresse beim Konfigurieren eine Verbindung zu einem beliebigen {{site.data.keyword.BluSoftlayer_notm}}-Rechenzentrum herstellen. Führen Sie die folgenden Schritte aus, um eine PPTP-VPN-Verbindung in Windows 7 aufzubauen.

## PPTP-VPN-Verbindung konfigurieren

1. Informationen zum Konfigurieren einer Fernverbindung finden Sie auf der [Seite mit den Vorgehensweisen](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} von Microsoft.

2. Geben Sie die Zieladresse des gewünschten Rechnungszentrums in das Feld für die Internetadresse ein. Die passenden Adressen für die aktuellen IBM Cloud-Rechenzentren finden Sie in der folgenden Tabelle.

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

3\. Geben Sie einen eindeutigen Namen für die Verbindung in das Feld **Zielname** ein.

**Hinweis:** Es wird empfohlen, den Standort des Rechenzentrums als Zielname zu verwenden.

4\. Geben Sie den Benutzernamen des [Kundenportals ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) in das Feld **Benutzername** ein.

5\. Geben Sie das **VPN-Kennwort** in das Feld **Kennwort** ein.

6\. Klicken Sie auf die Schaltfläche **Verbindung herstellen**.

7\. Jetzt müssen Sie auf dem Computer das ferne Gateway inaktivieren, damit Sie neben der VPN-Verbindung auch eine andere Verbindung ins Internet aufbauen können.

8\. Klicken Sie auf **Start**, öffnen Sie anschließend **Systemsteuerung** -> **Netzwerk- und Freigabecenter** -> **Adaptereinstellungen ändern**.

9\. Klicken Sie mit der rechten Maustaste auf die PPTP-VPN-Verbindung und klicken Sie auf **Eigenschaften**.

10\. Nehmen Sie die Auswahl des Kästchens 'TCP/IPv6' zurück, klicken Sie anschließend auf 'TCP/IPv4' und klicken Sie auf 'Eigenschaften'.

11\. Klicken Sie auf die Schaltfläche **Erweitert**.

12\. Nehmen Sie die Auswahl des Kästchens für **Standardgateway für das Remotenetzwerk verwenden** zurück und wählen Sie anschließend **OK** aus.

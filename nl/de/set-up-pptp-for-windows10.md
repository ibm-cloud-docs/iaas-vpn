---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# PPTP-VPN in Windows 10 konfigurieren

1. Starten Sie die Anwendung **Einstellungen** im Menü **Start** und klicken Sie auf **Netzwerk und Internet**.

2. Wählen Sie auf der linken Seite der Anzeige **Netzwerk und Internet** die Option **VPN** und auf der nachfolgenden Seite **VPN-Verbindung hinzufügen** aus.

![VPN-Verbindung hinzufügen](images/vpn1.png)

3. Auf der folgenden Seite konfigurieren Sie die PPTP-VPN-Verbindung. Dazu verwenden Sie die folgenden Einstellungen:

 * _VPN-Provider:_ Windows (integriert)
 * _Verbindung:_ Sie müssen für diese Verbindung einen Namen festlegen, zum Beispiel `MyPPTP`.
 * _Servername oder Adresse:_ Geben Sie den Namen des Servers ein, zu dem die Verbindung hergestellt werden soll. (Beispiel: `pptpvpn.dal01.softlayer.com`)
 * _VPN-Typ:_ Wählen Sie 'Point to Point Tunneling Protocol (PPTP)' aus.
 *_ Typ der Anmeldung:_ Wählen Sie 'Benutzername und Kennwort' aus.
  * Geben Sie jetzt VPN-Benutzername und -Kennwort ein.
  * Überprüfen Sie alle ausgewählten Daten noch einmal und klicken Sie auf **Speichern**.

![VPN-Einstellungen](images/vpn2.png)

4. Sobald wieder die VPN-Hauptseite angezeigt wird, wählen Sie die (von Ihnen davor erstellte) Verbindung `MyPPTP` aus, um eine Verbindung herzustellen.

![SoftLayer-PPTP](images/vpn3.png)

5. Wenn Sie das Internet verwenden möchten, während Sie verbunden sind, müssen Sie das ferne Gateway inaktivieren; dies kann über PowerShell durchgeführt werden.

 * Öffnen Sie PowerShell durch einen Rechtsklick auf PowerShell und die Auswahl von **Als Administrator ausführen**.
 * Geben Sie die folgenden Befehle ein:
 ```
`Get-VpnConnection`
`Set-VpnConnection -Name "MyPPTP" -SplitTunneling $True`
```

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configura la VPN PPTP in Windows 10

1. Avvia l'applicazione **Settings** dal menu **Start** e fai clic su **Network and Internet**.

2. Nel lato sinistro del pannello **Network and Internet**, seleziona **VPN** e nella seguente pagina, seleziona **Add a VPN Connection**.

![Aggiungi connessione VPN](images/vpn1.png)

3. Nella seguente pagina configurerai la tua connessione VPN PPTP. Queste sono le impostazioni:

 * _Provider VPN:_ Windows (integrato)
 * _Connessione:_ devi fornire un nome per questa connessione, ad esempio `MyPPTP`.
 * _Indirizzo o nome server:_ immetti il nome del server che vuoi raggiungere. (Ad esempio, `pptpvpn.dal01.softlayer.com`)
 * _Tipo di VPN:_ scegli "Point to Point Tunneling Protocol" (PPTP)
 *_ Tipo di accesso:_ scegli "User name and password"
  * Ora immetti i tuoi nome utente e password della VPN
  * Controlla ancora una volta tutti i dati selezionati e premi **Save**

![Impostazioni VPN](images/vpn2.png)

4. Dopo che sei di nuovo nella pagina della VPN principale, seleziona la connessione `MyPPTP` (che hai creato precedentemente) per collegarti.

![PPTP Softlayer](images/vpn3.png)

5. Per utilizzare internet mentre sei collegato, devi disabilitare il gateway remoto, puoi farlo con PowerShell.

 * Apri PowerShell facendo clic con il tasto destro su di esso e seleziona **Run As Administrator**
 * Immetti i seguenti comandi:
 ```
`Get-VpnConnection`
`Set-VpnConnection -Name "MyPPTP" -SplitTunneling $True`
```

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configura la VPN PPTP per Windows 7

La connessione VPN PPTP permette il collegamento remoto alla rete privata {{site.data.keyword.BluSoftlayer_notm}} da un desktop o un dispositivo dedicato. La connessione alla rete privata tramite PPTP è disponibile per più sistemi operativi, incluso Windows 7. Gli utenti possono collegarsi a un qualsiasi data center {{site.data.keyword.BluSoftlayer_notm}} immettendo l'indirizzo di destinazione univoco del data center al momento della configurazione.  Utilizza la seguente procedura per configurare una connessione VPN PPTP in Windows 7.

## Configura una connessione VPN PPTP 

1. Fai riferimento alla pagina [Procedure di Microsoft](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} per raggiungere la schermata per configurare la connessione remota.

2. Immetti l'indirizzo di destinazione del data center desiderato nel campo dell'indirizzo internet. Fai riferimento alla seguente tabella per gli indirizzi appropriati dei data center IBM Cloud correnti.

|Ubicazione data center|Indirizzo internet data center|
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
|Londra, GB|pptpvpn.lon02.softlayer.com|
|Parigi, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokyo, JP|pptpvpn.tok02.softlayer.com|

3\. Immetti un titolo descrittivo per la connessione nel campo **Destination name**.

**Nota:** ti consigliamo di utilizzare l'ubicazione del data center come nome di destinazione. 

4\. Immetti il tuo nome utente del [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) nel campo **User Name**.

5\. Immetti la tua **VPN Password** nel campo **Password**.

6\. Fai clic sul pulsante **Connect**.

7\. Ora, sul tuo computer, dovrai disabilitare il gateway remoto in modo da poterti collegare a internet così come alla VPN.

8\. Fai clic su **Start**, quindi apri **Control Panel** -> **Network and Sharing** -> **Change Adapter Settings**.

9\. Fai clic con il tasto destro sulla connessione VPN PPTP e fai clic su **Properties**.

10\. Deseleziona la casella TCP/IPv6 e fai clic su TCP/IPv4 e sulle proprietà.

11\. Fai clic sul pulsante **Advanced**.

12\. Deseleziona la casella per **Use Default Gateway on Remote Network** e seleziona **OK**.

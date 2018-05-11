---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione della VPN PPTP per Mac OS X 10.X

La connessione VPN PPTP permette il collegamento remoto alla rete privata {{site.data.keyword.BluSoftlayer_notm}} da un desktop o un dispositivo dedicato. La connessione alla rete privata tramite PPTP è disponibile per più sistemi operativi, incluso Mac OS X. Gli utenti possono collegarsi a un qualsiasi data center {{site.data.keyword.BluSoftlayer_notm}} immettendo l'indirizzo di destinazione univoco del data center al momento della configurazione.  Utilizza la seguente procedura per configurare una connessione VPN PPTP in Mac OS X.

## Configurazione di una connessione VPN PPTP

* Seleziona **System Preferences** dal menu a discesa **Apple Menu**.
* Fai clic sull'icona **Network** nella sezione Internet&Network . 
* Fai clic sull'icona **Plus Sign** alla fine del menu **Connections**.  Viene visualizzata una finestra a comparsa per farti creare la connessione VPN.
* Crea la connessione VPN.
  * Seleziona **VPN** dall'elenco a discesa **Interface**.
  * Seleziona **PPTP** dall'elenco a discesa **VPN Type**.
  * Immetti un **titolo descrittivo** per la connessione nel campo **Service Name**.
  * **Nota:** ti consigliamo di utilizzare l'ubicazione del data center come parte del nome del servizio.
  * Fai clic sul pulsante **Create**.
* Fai clic sulla connessione che è stata appena creata nel menu Connections.
* Immetti l'**indirizzo di destinazione** del data center desiderato nel campo **Server Address**.  Fai riferimento alla seguente tabella per gli indirizzi appropriati dei data center {{site.data.keyword.BluSoftlayer_notm}} correnti.
* Immetti il tuo **Customer Portal User Name** nel campo **Account name**.
* Completa le impostazioni di autenticazione.
  * Fai clic sul pulsante **Authentication Settings**.  Sarà visualizzata una casella a comparsa che richiede l'autenticazione alla VPN.
  * Immetti la tua **Customer VPN Password** nel campo **Password**.
  * Fai clic sul pulsante **OK**.
* Aggiorna le impostazioni del traffico VPN.
  * Fai clic sul pulsante **Advanced**.
  * Assicurati che la casella di spunta **Send all traffic over VPN Connection** nella sessione Session non sia selezionata.
  * Fai clic sul pulsante **OK**.
* Seleziona la casella di spunta **Show VPN Status in menu bar**.
* Fai clic sul pulsante Apply.  La connessione VPN può ora essere stabilita in qualsiasi momento utilizzando la voce della barra di menu VPN.

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

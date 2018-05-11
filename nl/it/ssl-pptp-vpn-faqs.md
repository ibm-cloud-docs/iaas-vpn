---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ VPN

## Cosa è una VPN IBM Cloud?

L'accesso VPN di IBM Cloud è progettato per consentire agli utenti di gestire in remoto tutti i server in modo sicuro nella rete privata di IBM Cloud.  Una connessione VPN dalla tua ubicazione alla rete privata consente la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato. Con l'accesso VPN, puoi:

* Stabilire una connessione VPN a una rete privata utilizzando SSL, PPTP o IPSEC
* Accedere al tuo server tramite il proprio indirizzo IP 10.x.x.x privato utilizzando SSH o RDP
* Collegarti all'indirizzo IP IPMI del tuo server per ulteriori bisogni di salvataggio o gestione server.


## La VPN SSL esegue anche PPTP, IPSEC o altri protocolli VPN?

Al momento il gateway VPN SSL utilizza un plugin VPN SSL basato sul browser o un client proprietario della creazione delle connessioni. Continueremo a portare ulteriori opzioni di connettività alla rete privata. La VPN SSL è stata selezionata per la semplicità di utilizzo e compatibilità.


<a name="152"></a>
## Posso montare il server NAS/FTP dalla mia ubicazione remota nel gateway della VPN SSL?

No...puoi solo avere accesso alla tua VLAN privata e ai tuoi server dal gateway della VPN SSL. Se desideri scaricare i dati dal tuo volume NAS/FTP, devi spostarli nel tuo server e poi dalla VPN all'ubicazione remota.

Per motivi di sicurezza, solo ai server ubicati nel data center è consentito l'accesso ai server che forniscono i servizi (DNS, Update, NAS, Lockbox).

<a name="175"></a>
## Quale fornitore ha creato la VPN SSL e come funziona?

Il nostro gateway della VPN SSL è un prodotto sicuro dalle reti di array.  Il gateway stesso viene eseguito in raggio per aggiornare gli utenti e le password dal nostro portale del cliente. Se desideri aggiungere gli utenti e fornirgli l'accesso VPN SSL, crea un nuovo utente nel portale del cliente e abilita le autorizzazioni VPN SSL.

<a name="276"></a>
## Quale è la differenza tra la VPN SSL e PPTP?

La **VPN SSL** consente a un utente di creare un tunnel sicuro da un desktop remoto alla rete privata {{site.data.keyword.BluSoftlayer_notm}}. È compatibile con molti sistemi operativi.

La **VPN PPTP** consente lo stesso tunnel sicuro ma si collega utilizzando il software del client specializzato a un dispositivo dedicato o al desktop di un utente. La VPN PPTP è un'ottima soluzione per gli utenti che non possono utilizzare la connessione SSL.

## Quando mi collego a una VPN PPTP, visualizzo "Error 691: Access was denied because the username and/or password is invalid." Come posso risolvere il problema?

Tutti gli utenti hanno la possibilità di collegarsi alla VPN PPTP, ma devono avere l'autorizzazione ad accedere tramite il portale del cliente.  Le autorizzazioni della VPN PPTP vengono verificate facilmente e aggiornate velocemente.  Fai riferimento a [Attiva o disattiva l'accesso VPN PPTP](activate-a-user.html) per ulteriori informazioni.

## Perché non sono in grado di aggiungere ulteriori utenti alla VPN PPTP?

La VPN PPTP è disponibile per tutti gli account, ma è inizialmente configurata per abilitare l'accesso di un utente alla volta. Per richiedere l'abilitazione di un account per PPTP illimitati senza costi aggiuntivi, crea un ticket tramite il [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) con le seguenti informazioni, insieme a tutti i dettagli aggiuntivi che possono essere necessari:

* Argomento: richiesta VPN PPTP
* Testo: al momento ho PPTP limitato a un utente alla volta. Abilitare l'accesso VPN PPTP illimitato per il mio account.

Un membro del team di supporto di IBM aggiornerà l'account per abilitare l'accesso PPTP illimitato, il quale è disponibile gratuitamente. Il ticket sarà aggiornato se sono necessarie ulteriori informazioni.

## Quali sono le categorie disponibili per uno stato di gestione della VPN dell'utente nel portale del cliente? 

Le categorie dello stato del cliente includono quelle che possono essere aggiornate da un utente e quelle che possono essere visualizzate automaticamente. Includono:

* **Attivo** - L'utente ha accesso al [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) e alla VPN basata sulle autorizzazioni configurate dall'amministratore dell'account. Questo stato può essere selezionato manualmente o modificato in qualsiasi momento. 
* **Disabilitato** - L'utente non ha accesso a tutte le autorizzazioni e sottoscrizioni nell'account, incluso il [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) e la VPN. Se impostato su disabilitato da un altro utente nell'account, questo stato può essere selezionato manualmente e/o modificato in qualsiasi momento.
* **Solo VPN** - L'utente ha solo l'accesso alla connettività VPN e non può accedere al [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Questo stato può essere selezionato manualmente o modificato in qualsiasi momento. 
* **Inattivo** - L'utente non ha utilizzato il [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) o la VPN negli ultimi 60 giorni. Questo è uno stato generato dal sistema.
* **annullamento in attesa** - Un amministratore dell'account ha eliminato questo utente e l'annullamento è al momento in fase di elaborazione. Questo è uno stato generato dal sistema. 

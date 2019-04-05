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

# FAQ VPN
{:#vpn-faq}

## Cosa è una VPN IBM Cloud?
{:#what-is-ibm-cloud-vpn}
{:faq}

L'accesso VPN di IBM Cloud è progettato per consentire agli utenti di gestire in remoto tutti i server in modo sicuro nella rete privata di IBM Cloud.  Una connessione VPN dalla tua ubicazione alla rete privata consente la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato. Con l'accesso VPN, puoi:

* Stabilire una connessione VPN alla rete privata utilizzando SSL o IPSEC
* Accedere al tuo server tramite il proprio indirizzo IP 10.x.x.x privato utilizzando SSH o RDP
* Connetterti all'indirizzo IP IPMI del tuo server per ulteriori esigenze di salvataggio o gestione server.


## La VPN SSL esegue anche PPTP, IPSEC o altri protocolli VPN?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Al momento il gateway VPN SSL utilizza un plugin VPN SSL basato sul browser o un client proprietario della creazione delle connessioni. Continueremo a portare ulteriori opzioni di connettività alla rete privata. La VPN SSL è stata selezionata per la semplicità di utilizzo e compatibilità. PPTP è obsoleto. Per ulteriori informazioni, vedi [Deprecazione VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).



## Posso montare il server NAS/FTP dalla mia ubicazione remota nel gateway della VPN SSL?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

No...puoi solo avere accesso alla tua VLAN privata e ai tuoi server dal gateway della VPN SSL. Se desideri scaricare i dati dal tuo volume NAS/FTP, devi spostarli nel tuo server e poi dalla VPN all'ubicazione remota.

Per motivi di sicurezza, solo ai server ubicati nel data center è consentito l'accesso ai server che forniscono i servizi (DNS, Update, NAS, Lockbox).


## Quale fornitore ha creato la VPN SSL e come funziona?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Il nostro gateway della VPN SSL è un prodotto sicuro dalle reti di array.  Il gateway stesso viene eseguito in raggio per aggiornare gli utenti e le password dal nostro portale del cliente. Se desideri aggiungere gli utenti e fornirgli l'accesso VPN SSL, crea un nuovo utente nel portale del cliente e abilita le autorizzazioni VPN SSL.


## Qual è la differenza tra la VPN SSL e PPTP?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

La **VPN SSL** consente a un utente di creare un tunnel sicuro da un desktop remoto alla rete privata {{site.data.keyword.BluSoftlayer_notm}}. È compatibile con molti sistemi operativi.

La **VPN PPTP** consente lo stesso tunnel sicuro ma si connette utilizzando il software del client specializzato sul desktop o dispositivo dedicato di un utente. Tuttavia, PPTP è obsoleto. Per ulteriori informazioni, vedi [Deprecazione VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Perché non sono in grado di aggiungere ulteriori utenti alla VPN PPTP?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP è obsoleto. Per ulteriori informazioni, vedi [Deprecazione VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Quali sono le categorie disponibili per uno stato di gestione della VPN dell'utente nel portale del cliente?
{:#what-are-available-categories-vpn-management}
{:faq}

Le categorie dello stato del cliente includono quelle che possono essere aggiornate da un utente e quelle che possono essere visualizzate automaticamente. Includono:

* **Attivo** - L'utente ha accesso al [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) e alla VPN basata sulle autorizzazioni configurate dall'amministratore dell'account. Questo stato può essere selezionato manualmente o modificato in qualsiasi momento.
* **Disabilitato** - L'utente non ha accesso a tutte le autorizzazioni e sottoscrizioni nell'account, incluso il [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) e la VPN. Se impostato su disabilitato da un altro utente nell'account, questo stato può essere selezionato manualmente e/o modificato in qualsiasi momento.
* **Solo VPN** - L'utente ha solo l'accesso alla connettività VPN e non può accedere al [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Questo stato può essere selezionato manualmente o modificato in qualsiasi momento.
* **Inattivo** - L'utente non ha utilizzato il [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) o la VPN negli ultimi 60 giorni. Questo è uno stato generato dal sistema.
* **annullamento in attesa** - Un amministratore dell'account ha eliminato questo utente e l'annullamento è al momento in fase di elaborazione. Questo è uno stato generato dal sistema.

## Come configuro la VPN SSL?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

Per istruzioni dettagliate, vedi [Connessione alla VPN SSL - Windows 7 e superiore](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



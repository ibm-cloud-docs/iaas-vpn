---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: IPSec VPN, IP address, IP traffic

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configura la VPN IPSec
{:#setup-ipsec-vpn}

## Cosa è la VPN IPSec?
{:#what-is-ipsec-vpn}

IPSec è una suite di protocolli progettata per autenticare e codificare tutto il traffico IP tra due ubicazioni, utilizzando una modalità di tunneling che fornisce una rete codificata site-to-site. Consente ai dati attendibili di passare tramite le reti che altrimenti sarebbero considerati non sicuri.   Per ulteriori informazioni generali su IPSec, fai riferimento alla [documentazione di riferimento](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation).


L'accesso VPN di IBM Cloud consente agli utenti di gestire tutti i server in remoto e in modo sicuro nella rete privata di IBM Cloud.  Una connessione VPN dalla tua ubicazione alla rete privata fornisce la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato.  Con l'accesso VPN, puoi:

   * Stabilire una connessione VPN alla rete privata attraverso SSL o IPSEC
   * Accedere al tuo server tramite il proprio indirizzo IP 10.x.x.x privato attraverso SSH o RDP
   * Connetterti all'indirizzo IP IPMI del tuo server per ulteriori esigenze di salvataggio o gestione server.

Forniamo il servizio IPSec ai clienti per la gestione dei loro ambienti. Non è consigliato per i carichi di lavoro nella produzione.


## Configurazione di una connessione IPSec
{:#setup-ipsec-connection}

### Parametri di negoziazione
{:#setup-ipsec-vpn-negotiation-parameters}
![Parametri di negoziazione](images/IPSec_VPN.png)

Dovrai conoscere le seguenti informazioni per il lato remoto della VPN IPSec:
- Indirizzo IP statico dell'endpoint VPN
- Chiave precondivisa (Password)
- Algoritmo di codifica (DES, 3DES, AES128, AES192, AES256)
- Autenticazione (MD5, SHA1, SHA256, per la fase 1&2)
- Gruppo Diffie-Hellman (per la fase 1&2)
- Viene utilizzato PFS (perfect forward secrecy)?
- Ora keylife (per la fase 1 & 2) - **NOTA:** il nostro sistema misura questo valore in secondi!

Una volta che disponi di queste informazioni, puoi configurare i parametri di negoziazione di base della connessione VPN.

### Reti protette
{:#setup-ipsec-vpn-protected-networks}

Nelle proprietà della connessione VPN, devi definire le reti nel lato remoto del tunnel nonché le reti locali del tunnel. In “Protected Customer (Remote) Subnet”, immetti lo spazio dell'indirizzo IP privato nell'annotazione CIDR per il lato remoto (non IBM) del tunnel IPSec.

<span style="text-decoration: underline">Ad esempio:</span> se la tua rete nel lato remoto del tunnel utilizza una sola sottorete 10.0.0.0 con una maschera di rete 255.255.255.0, devi immettere l'indirizzo IP 10.0.0.0 / CIDR 24 per la sezione “Protected Customer (Remote) Subnet”.

### NAT (Network Address Translation)
{:#setup-ipsec-vpn-nat}

Con la VPN IPSec, puoi anche definire gli indirizzi IP privati nella rete {{site.data.keyword.BluSoftlayer_notm}} che instraderanno il traffico alle sottoreti remote nell'altro lato della connessione VPN.  Questo ti consente di avere il traffico internet privato instradato a uno degli indirizzi IP interni di una macchina dietro la tua VPN, senza esporre l'ubicazione remota all'accesso internet completo.  

### Sottoreti Network Address Translation/NAT statiche assegnate
{:#setup-ipsec-vpn-nat-static-subnets}

Per configurare un IP VPN remoto con una voce NAT statica: 

 * Seleziona la freccia rossa per visualizzare l'elenco delle sottoreti nella sezione **Assigned Static NAT subnets**. Sarà visualizzato ogni IP nella sottorete.  
 * Immetti l'IP nel lato remoto della connessione VPN nella colonna **Customer IP** e inserisci un nome per l'associazione nella colonna **Name**.  
 * Seleziona **Add/Modify Context Address Translations** e **Apply Configurations** per salvare e applicare la configurazione.
 
Questa azione configura una traduzione della rete one-to-one per il traffico restituito, che viene utilizzata dai tuoi host dietro a un concentratore VPN di IBM Cloud per comunicare con gli host dietro il peer VPN remoto. Ad esempio, tutto il traffico dell'IP 10.1.255.92 sarà tradotto e instradato all'IP del cliente 192.168.10.15. Questo inoltro elimina il bisogno di ulteriori voci di instradamento al server IBM Cloud.

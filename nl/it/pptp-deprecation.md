---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Deprecazione VPN PPTP
{:#pptp-vpn-deprecation}

La VPN PPTP è stata dichiarata obsoleta a partire dal 12 giugno 2018 e non è più offerta ai clienti. Grazie per l'interesse. Per scoprire alcune possibili alternative, continua a leggere.

## Cosa è la VPN?
{:#pptp-vpn-deprecation-what-is-vpn}
L'accesso VPN abilita gli utenti a gestire tutti i server in remoto e in modo sicuro nella rete privata di IBM Cloud. Una connessione VPN dalla tua ubicazione alla rete privata consente la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato. Con l'accesso VPN, puoi:

* Stabilire una connessione VPN a una rete privata da SSL, **PPTP** o IPSec
* Accedere al tuo server utilizzando il proprio indirizzo IP 10.x.x.x privato da SSH o RDP
* Connetterti all'indirizzo IP IPMI del tuo server per ulteriori esigenze di salvataggio o gestione server

## Deprecazione PPTP
{:#pptp-deprecation-vpn}
Poiché altre opzioni VPN diventano più sicure e versatili, la necessità di PPTP è diminuita. {{site.data.keyword.BluSoftlayer_notm}} fornisce diverse altre opzioni, come SSL o IPSec, che sono più sofisticate e protettive rispetto a PPTP.

**Per questi motivi, {{site.data.keyword.BluSoftlayer_notm}} non offre più PPTP a partire dal 12 giugno 2018.**
{:important}


## Domande frequenti (FAQ)
{:#pptp-vpn-deprecation-faq}

**D: perché PPTP è diventato obsoleto?**

**R:** per fornire la massima protezione, {{site.data.keyword.BluSoftlayer_notm}} ha interrotto l'utilizzo di PPTP. {{site.data.keyword.BluSoftlayer_notm}} desidera confermare la promessa ai nostri clienti che la protezione dei loro dati e della loro privacy sia di estrema importanza. 

**D: quali altri tipi di accesso VPN sono disponibili oltre a PPTP?**

**R:** {{site.data.keyword.BluSoftlayer_notm}} offre diverse opzioni che richiedono solo una semplice configurazione.
  1. La VPN SSL è una connessione ad accesso rapido che ti connette alla nostra rete privata direttamente da un browser. La VPN SSL è compatibile con Windows XP o successivo e ActiveX, Fedora, Ubuntu e Mac OSX. L'accesso globale alla nostra rete è disponibile con un solo URL, che ti consente di scegliere l'endpoint VPN più vicino. Consulta [Configura le connessioni VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) per ulteriori dettagli sull'introduzione a questa opzione.
  2. IPSec è una suite di protocolli progettata per autenticare e codificare tutto il traffico IP tra due ubicazioni. Consente ai dati attendibili di passare tramite le reti che altrimenti sarebbero considerati non sicuri. Per ulteriori informazioni generali su IPSec, fai riferimento a [Configura la VPN IPSec](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) e all'altra [documentazione di riferimento](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation) per iniziare ad utilizzare questo servizio. 

**D: se le mie procedure di business necessitano di PPTP?**

**R:** sono disponibili molte opzioni se PPTP è necessario per le tue esigenze aziendali. **Non tutte le opzioni possibili sono qui incluse. Tieni presente che le seguenti opzioni richiedono la configurazione completa di entrambi gli endpoint. Il cliente è responsabile della configurazione di queste opzioni.**
  1. VRA (Virtual Router Appliance). Il VRA (Virtual Router Appliance), conosciuto anche come Vyatta, funge da gateway e router per il tuo ambiente. Contiene zone formate da sottoreti. Le regole del firewall vengono implementate tra le zone in modo che possano comunicare tra di loro. Per le zone che non devono comunicare tra di loro, non è necessaria alcuna regola del firewall poiché tutti i pacchetti verranno eliminati. Fai riferimento a [Introduzione a VRA (Virtual Router Appliance)](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance) per ulteriori dettagli sull'introduzione a questo servizio. 
  2. Firewall FSA. Il FortiGate Security Appliance (FSA) 10Gbps è un firewall hardware che può essere configurato per proteggere il traffico su più VLAN per le reti privata e pubblica. Nel portale del cliente viene indicato come un “Firewall a più VLAN”. Fai riferimento a [Introduzione a FSA 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) per ulteriori dettagli sull'introduzione a questo servizio. 
 
Le opzioni precedenti sono alcune possibilità che puoi esplorare se PPTP è necessario per le tue esigenze aziendali, dopo che il servizio non viene più fornito da {{site.data.keyword.BluSoftlayer_notm}}. Ti ringraziamo per il tuo business.
{:note}

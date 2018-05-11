---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni sulla VPN

L'accesso VPN ti consente di gestire tutti i server e i servizi associati al tuo account, in remoto, in una rete privata IBM Cloud. Una connessione VPN dalla tua ubicazione alla rete privata consente la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato.

La comunicazione utilizzando la rete privata è intrinsecamente più sicura. Ti fornisce la flessibilità per limitare l'accesso pubblico mentre ancora sei in grado di gestire i tuoi server. È possibile fornire l'accesso VPN a tutti gli utenti nel tuo account, il quale è disponibile tramite SSL e PPTP. Le interazioni VPN tramite il [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) consentono la personalizzazione dell'accesso VPN al livello dell'utente.

## Quali sono alcuni modi di utilizzare la VPN SSL?

Questo gateway sicuro fuori banda ti fornisce l'accesso al tuo server nella rete privata. Gli utilizzi comuni sono:

* Collegamento all'indirizzo IP privato del tuo server (10.x.x.x) per SSH o RDC.
* Collegamento alla tua scheda IPMI per console/accesso/monitoraggio remoti.
* Montaggio delle unità in Windows o Red Hat dal PC di casa o del lavoro per praticità.
* Arresto dell'interfaccia pubblica sui server database e gestione nella rete privata.
* Arresto dell'interfaccia pubblica mentre configuri il server per la prima volta.
* Arresto dell'interfaccia pubblica durante gli aggiornamenti di sicurezza critici. 
* Arresto dell'interfaccia pubblica durante una violazione della sicurezza e la risoluzione del problema nella rete privata. 

## Funzioni chiave

 * La nostra rete privata ti fornisce un modo gratuito di comunicare e gestire i server. La VPN è il gateway a questa rete privata.
 * Offriamo le opzioni VPN SSL e PPTP.
 * I punti di accesso nel mondo creano l'accesso e l'interazione migliori e più veloci possibile. IBM Cloud al momento ha punti di accesso VPN in molte città.
 * Visita http://www.softlayer.com/vpn-access per un elenco di punti di accesso VPN alla rete privata {{site.data.keyword.BluSoftlayer_notm}}.

## Come funziona

Con l'accesso VPN, esistono due modi per collegarti alla rete privata e per gestire i tuoi server e servizi. Queste opzioni includono le connessioni VPN SSL e PPTP. Collegati alla rete privata utilizzando entrambi i metodi, in base alle tue preferenze o bisogni personali.
 
## Connessioni VPN SSL

La VPN SSL è una connessione di accesso rapido che ti collega alla nostra rete privata direttamente da un browser. La VPN SSL è compatibile con Windows XP o successivo e ActiveX, Fedora, Ubuntu e Mac OSX. L'accesso globale alla nostra rete è disponibile con un solo URL, che ti consente di scegliere l'endpoint VPN più vicino.

## Limite sottorete VPN SSL

Il client VPN SSL ha un limite forzato di 64 sottoreti che può essere utilizzato per popolare la sua tabella di instradamento. Se il tuo account ha più di 64 sottoreti, assicurati di modificare le tue autorizzazioni VPN SSL per utilizzare l'assegnazione della sottorete manuale. Se non fai ciò, alcune sottoreti diventeranno irraggiungibili tramite la VPN SSL.

## Connessioni VPN PPTP

La VPN PPTP ti consente di collegarti alla rete privata in modo sicuro, utilizzando il software client specifico del SO dal tuo desktop o utilizzando un dispositivo dedicato con un firewall o un router. Al momento forniamo la connettività VPN per Windows XP o successivo, Fedora, Ubuntu e Mac OSX. L'opzione di connessione VPN PPTP è progettata per chi intende collegare un intero ufficio o per chi non può collegarsi utilizzando l'opzione VPN SSL. Le connessioni PPTP sono stabilite con un solo data center che può essere scelto quando viene configurata la connessione VPN.

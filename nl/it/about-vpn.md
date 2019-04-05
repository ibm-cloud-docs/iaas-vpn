---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni sulla VPN
{:#about-iaas-vpn}

L'accesso VPN ti consente di gestire tutti i server e i servizi associati al tuo account, in remoto, in una rete privata IBM Cloud. Una connessione VPN dalla tua ubicazione alla rete privata consente **la gestione fuori banda e il salvataggio del server** tramite un tunnel VPN codificato.

La comunicazione utilizzando la rete privata è intrinsecamente più sicura. Ti fornisce la flessibilità per limitare l'accesso pubblico mentre ancora sei in grado di gestire i tuoi server. È possibile fornire l'accesso VPN a tutti gli utenti nel tuo account, il quale è disponibile tramite SSL. Le interazioni VPN tramite il [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) consentono la personalizzazione dell'accesso VPN al livello dell'utente.

## Quali sono alcuni modi di utilizzare la VPN SSL?
{:#ways-to-use-iaas-vpn}

Questo gateway sicuro fuori banda ti fornisce l'accesso al tuo server nella rete privata. Gli utilizzi comuni sono:

* Connessione all'indirizzo IP privato del tuo server (10.x.x.x) per SSH o RDC.
* Connessione alla tua scheda IPMI per console/accesso/monitoraggio remoti.
* Montaggio delle unità in Windows o Red Hat dal PC di casa o del lavoro per praticità.
* Arresto dell'interfaccia pubblica sui server database e gestione nella rete privata.
* Arresto dell'interfaccia pubblica mentre configuri il server per la prima volta.
* Arresto dell'interfaccia pubblica durante gli aggiornamenti di sicurezza critici.
* Arresto dell'interfaccia pubblica durante una violazione della sicurezza e la risoluzione del problema nella rete privata.

## Funzioni chiave
{:#iaas-vpn-key-features}

 * La nostra rete privata ti fornisce un modo gratuito di comunicare e gestire i server. La VPN è il gateway a questa rete privata.
 * I punti di accesso nel mondo creano l'accesso e l'interazione migliori e più veloci possibile. IBM Cloud al momento ha punti di accesso VPN in molte città.
 * Visita http://www.softlayer.com/vpn-access per un elenco di punti di accesso VPN alla rete privata {{site.data.keyword.BluSoftlayer_notm}}.

## Come funziona
{:#iaas-vpn-how-it-works}

Con l'accesso VPN, utilizza SSL per connetterti alla rete privata e per gestire i tuoi server e servizi. 

## Connessioni VPN SSL
{:#iaas-vpn-ssl-vpn-connections}

La VPN SSL è una connessione ad accesso rapido che ti connette alla nostra rete privata direttamente da un browser. La VPN SSL è compatibile con Windows XP o successivo e ActiveX, Fedora, Ubuntu e Mac OSX. L'accesso globale alla nostra rete è disponibile con un solo URL, che ti consente di scegliere l'endpoint VPN più vicino.

## Limite di sottoreti VPN SSL
{:#iaas-vpn-ssl-vpn-subnet-limit}

Il client VPN SSL ha un limite forzato di 64 sottoreti che può essere utilizzato per popolare la sua tabella di instradamento. Se il tuo account ha più di 64 sottoreti, assicurati di modificare le tue autorizzazioni VPN SSL per utilizzare l'assegnazione della sottorete manuale. Se non fai ciò, alcune sottoreti diventeranno irraggiungibili tramite la VPN SSL.

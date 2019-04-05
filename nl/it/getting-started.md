---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, IBM Cloud VPN, user account

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Introduzione alla VPN (Virtual Private Networking)
{:#gettingstarted-with-virtual-private-networking}

## Cosa è una VPN IBM Cloud?
{:#what-is-ibmcloud-vpn}


L'accesso VPN abilita gli utenti a gestire tutti i server in remoto e in modo sicuro nella rete privata di IBM Cloud. Una connessione VPN dalla tua ubicazione alla rete privata consente la gestione fuori banda e il salvataggio del server tramite un tunnel VPN codificato. Con l'accesso VPN, puoi:

* Stabilire una connessione VPN a una rete privata mediante SSL o IPSec.
* Accedere al tuo server tramite il proprio indirizzo IP 10.x.x.x privato da SSH o RDP.
* Connetterti all'indirizzo IP IPMI del tuo server per ulteriori esigenze di salvataggio o gestione server.

**I servizi VPN PPTP sono diventati obsoleti a partire dal 12 giugno 2018, come descritto nel [nostro annuncio](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).**
{:deprecated}

Diversi servizi richiedono l'accesso tramite la rete privata e la VPN è un metodo che consente l'accesso alla rete privata. L'utilizzo di una VPN è utile quando hai bisogno di accedere alla rete privata, lavorare e poi scollegarti. Ad esempio, questo accesso spesso è necessario per raggiungere il KVM del server.

Ad ogni account utente può essere fornito l'accesso VPN e può essere limitato riguardo le sottoreti a cui deve accedere. Devi avere l'accesso VPN abilitato e devi creare una password VPN prima di poter accedere alla VPN.

## Abilita l'accesso VPN di ogni utente
{:#enable-user-vpn-access}

Per iniziare, dovrai abilitare l'accesso VPN per ogni account che ne ha bisogno. Ogni account all'inizio ha l'accesso VPN **disabilitato**, incluso l'account master del tuo team. Per abilitare l'accesso VPN, segui questa procedura:

1. Vai a **Account -> VPN Access** nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/).
* Troverai la riga di ogni utente VPN possibile e un link nella colonna **VPN Access**.
* Il link leggerà "None" se l'utente non ha ancora l'accesso VPN abilitato.
* Se il link dell'accesso VPN dell'utente legge **SSL**, significa che l'utente già ha il proprio accesso VPN abilitato.

![Tabella accesso VPN portale Softlayer](images/vpnaccess01.png)

1. Per abilitare o modificare i tipi di accesso VPN consentiti a un utente specifico, fai clic sul link nella colonna **VPN Access**.
* Nella pagina successiva puoi abilitare il tipo di accesso VPN appropriato per ogni utente.  

![Assegna il tipo di accesso VPN a un utente](images/vpntype01.png)

## Configura la password VPN
{:#set-vpn-password}

Il tuo prossimo passo è di creare una password VPN. Ogni utente può creare e aggiornare la propria password nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Per far ciò, seleziona il tuo nome in alto a destra, vieni portato alla pagina **Edit profile**. Puoi anche selezionare **Account -> Users** e poi il tuo nome utente.

      Nota: il link legge "Master User". Questo link leggerà il tuo nome per gli utenti secondari.

Nella pagina **Edit User Profile**, scorri semplicemente in basso e inizializza o aggiorna la password VPN.

![Campi password VPN Edit Profile](images/vpnpasswordfields.png)

## Accedi alla VPN
{:#login-to-the-vpn}

Ora che l'accesso VPN è stato stabilito, puoi accedere.

1. Per accedere alla VPN SSL, visita [vpn.softlayer.com](https://vpn.softlayer.com/) e seleziona uno dei punti di accesso. Puoi utilizzare qualsiasi punto di accesso VPN e ti vengono fornite le stesse autorizzazioni di accesso alla rete privata in tutti i data center.
* Se hai problemi nell'accesso a un'ubicazione, provane un'altra.
* In alternativa, puoi accedere utilizzando una VPN SSL client autonoma.

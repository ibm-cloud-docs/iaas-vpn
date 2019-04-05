---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Linux Fedora, SSL VPN connections Windows, backend IP address

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configura le connessioni VPN SSL
{:#setup-ssl-vpn-connections}

Windows, Linux Fedora e Linux richiedono istruzioni di connessione personalizzate, che vengono illustrate in questo documento. Questi sono alcuni esempi di come puoi utilizzare una connessione VPN SSL:

* Collegati con il desktop remoto all'indirizzo IP di backend del tuo server (10.4.X.X) per la gestione dei tuoi server Windows 2003.
* Esegui SSH all'indirizzo IP di backend del tuo server (10.4.X.X) per la gestione dei tuoi server UNIX.
* Utilizza un client IPMI per controllare il tuo server utilizzando l'indirizzo IPMI di backend (10.4.X.X). Puoi scaricare lo strumento client IPMI una volta connesso andando all'indirizzo http://downloads.softlayer.local/ipmi/ (devi essere connesso alla VPN privata SoftLayer).
  * **Nota:** IPMIView richiede che sia installato Java.  http://www.sun.com/java/
* Verifica il tuo sito web negli IP di backend prima di portarlo live nei tuoi IP pubblici.
* Trasferisci i file dei dati protetti tra i tuoi server e i tuoi casa/ufficio.
* Esegui il backup dei file di configurazione dei tuoi server nei tuoi casa/ufficio.
* Connettiti in modo sicuro al nostro [Portale web](http://control.softlayer.com/).

## Windows (Internet Explorer)
{:#setup-ssl-vpn-connections-windows}

1. Apri Internet Explorer e vai all'indirizzo `http://www.softlayer.com/vpn-access`.
* Una volta immessi i tuoi nome utente e password, ti sarà richiesto di installare un plugin ActiveX. Devi installare questo plugin per connetterti alla tua rete di backend. 
* Devi anche disporre dei diritti amministrativi nella tua workstation per installare il plugin ActiveX. Se non hai i diritti per installare il plugin, chiedi al tuo amministratore di sistema locale di installarlo al tuo posto. 
* Una volta che il plugin ActiveX è installato, un connettore di rete Array SSL VPN avvia e stabilisce una connessione al dispositivo VPN. Se ha avuto esito positivo, viene visualizzata una '**A**' rossa nella tua barra delle attività. Puoi fare clic sulla '**A**' in qualsiasi momento per visualizzare lo stato della tua connessione VPN SSL: lo stato, l'indirizzo IP assegnato, i server DNS assegnati, le rotte di rete e il tempo della connessione. 
* Puoi ridurre la tua sessione browser in qualsiasi momento e continuare ad utilizzare le altre applicazioni in modo sicuro nella rete privata. 
* Una volta che hai finito, scollegati selezionando il pulsante di disconnessione alla destra o semplicemente chiudi la finestra.

## Linux Fedora 
{:#setup-ssl-vpn-connections-linux}

Firefox non supporta più i plug-in NPAPI (applet java). Utilizza un browser diverso per eseguire questi passi.
{:note}

Si consiglia di eseguire tutti i comandi come root. (`setuid root`)

1. Scarica Java da `http://java.com/en/download/manual.jsp`. Questo è un file autoestraente di Linux.
* Chiudi il tuo browser.
* Sposta il file dove vuoi per installare Java (normalmente in `/usr/local`)
* Rendi il file eseguibile utilizzando il comando `chmod +x jre-6u1-linux-i586.bin`
* Esegui il programma di installazione utilizzando il comando `./jre-6u1-linux-i586.bin`
* Accetta i termini e installa.
* Dopo aver terminato l'installazione devi creare un collegamento simbolico.

## Esempio Linux
{:#setup-ssl-vpn-connections-linux-example}

1. Apri il tuo browser e vai all'indirizzo `http://www.softlayer.com/vpn-access`.
* Accedi con i tuoi nomi utente e password del portale del cliente.
* Una volta connesso, seleziona la scheda **Network**.
* Dovresti vedere un pulsante di connessione/installazione. Selezionalo e ti dovrebbe venir richiesto di installare un componente Java.
* Lascia il componente installarsi nel percorso predefinito, che potresti dover creare manualmente. (`/usr/local/array_vpn`)
* Dopo che è stato installato, dovrebbe venire visualizzata una finestra che mostra che sei connesso.
* Questa finestra deve rimanere aperta per utilizzare il tunnel VPN, ma puoi ridurla.
* Per verificare la connessione, esegui il ping di 10.0.80.11 o dell'indirizzo privato del tuo server. Se ricevi una risposta, sei connesso correttamente.
* Quando hai finito, seleziona il pulsante di disconnessione nella scheda 'Network' o semplicemente chiudi tutte le tue finestre del browser.

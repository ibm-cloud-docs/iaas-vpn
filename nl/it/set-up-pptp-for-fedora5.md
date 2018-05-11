---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configura PPTP per Fedora Core 5

Dovrai installare e configurare.

**1. Installazione**
Installa PPTP e la GUI `pptpconfig` utilizzando uno dei seguenti comandi:
```
# rpm -Uvh http://pptpclient.sourceforge.net/yum/stable/fc5/pptp-release-current.no...
# yum --enablerepo=pptp-stable install pptpconfig
```

**2. Configurazione**

1. Informazioni su IBM Cloud PPTP:
<table><tr><td>Server:</td><td>pptpvpn.dal01.softlayer.com (Dallas)<br/>pptpvpn.sea01.softlayer.com (Seattle)<br/>pptpvpn.wdc01.softlayer.com (Washington D.C.)</td></tr><tr><td>Nome dominio:</td><td>Lasciare vuoto</td></tr><tr><td>Nome utente:</td><td>(esempio: SL12345)</td></tr><tr><td>Password:</td><td>&nbsp;</td></tr></table>

2. Esegui *pptpconfig* <span style="text-decoration: underline">come root</span> e dovrebbe essere visualizzata una finestra,<br/>
![Figura 1](images/ss1.jpeg)

3. Immetti il nome, il server, il nome utente e la password nella scheda Server.

4. Nella sezione Encryption lascia tutto sui valori predefiniti, il che funziona per la maggior parte dei clienti.<br/>
![Figura 2](images/ss2.jpeg)

5. Fai clic su *Add* e il tunnel sarà visualizzato nell'elenco,

6. Fai clic sul tunnel per selezionarlo e poi su *Start*, sarà visualizzata una finestra con lo stato e i log della connessione tunnel,

7. Se la connessione non riesce, potresti aver bisogno di ulteriori informazioni, per cui nella scheda *Miscellaneous*, fai clic su *Enable connection debugging facilities*, su *Update*, riprova *Start*, quindi guarda [Diagnosis HOWTO](http://pptpclient.sourceforge.net/howto-diagnosis.phtml){:new_window} se viene visualizzato un errore.<br/>
![Figura 3](images/ss3.jpeg)

8. Se la connessione ha esito positivo, puoi provare il pulsante di test Ping. Se il ping ha esito negativo, dovresti provare a capire perché prima di procedere. Se il ping funziona, il tunnel è attivo e puoi ora utilizzare l'instradamento.

9. Solo gli IP che sono live nella rete di backend in IBM Cloud dovrebbero essere instradati in questo tunnel VPN.  *Arresta* il tunnel, selezionalo nuovamente, poi fai clic su *Client to LAN or LAN to LAN* nella scheda *Routing*, utilizza il pulsante *Edit Network Routes* per immettere '10.0.0.0/8' per la rete e 'SoftLayer' per il nome e riprova *Start*. Ora prova ad accedere all'indirizzo IP privato del tuo server o al server del nome privato di SoftLayer con 10.0.80.11.<br/>
![Figura 4](images/ss4.jpeg)

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Client VPN autonomi - Windows, Linux e Mac OS X

## Cliente autonomo Windows

Windows (8/7/Vista/XP) 32-bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) 64-bit:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. Scarica uno dei file elencati precedentemente, a seconda del tuo sistema operativo.
* Esegui MotionProSetup per installare il software.
* Esegui MotionPro e all'apertura della schermata seleziona **Profile -> Add**.
* Crea un profilo fornendo un nome del sito, scegliendo un nome host dall'elenco dei siti VPN SSL (sottostante). Immetti quindi i tuoi nome utente e password della VPN e premi **Save**.
* Infine, fai doppio clic sul profilo appena creato per collegarti alla VPN.

**Note**
 * 'Site' può essere un nome del dominio o un indirizzo IP.
 * Se hai problemi, disinstalla tutti i programmi dell'array utilizzando il pannello di controllo di Windows, riavvia, quindi ricollegati.
 * Non funziona con Windows 8 RT.

## Cliente autonomo Linux

CentOS 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat 32-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64-bit: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. Rendilo eseguibile:`chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* Esegui lo script:  `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh.`
* Sintassi:  `./MotionPro --host [site] --user [username] --passwd [password]`
* Per arrestarlo:  `[control-c]`

**Note:**  
 * Per avviare il client MotionPro, devi immetter almeno `hostname` e `username` come argomenti.
 * 'Site' può essere un nome del dominio o un indirizzo IP.

## Cliente autonomo Mac OS X 10.10

Procedura per il client MacOS StandAlone Array SSL VPN Motion Pro Plus:

1. Installa il client "Motion Pro Plus" dal negozio Apple. 
* Individua il client Motion Pro Plus nella cartella delle applicazioni e apri l'applicazione.
* Fai clic su 'Profile' e poi su 'Add'. 
* Riempi Site Name, Host e Username, quindi fai clic su Ok. 
* Fai clic sulla VPN in alto a sinistra, quindi collegati.

Può essere trovato un esempio con quanto segue:

![Figura 1](images/snip20170425_1.png)

Se il tunnel non indirizza il traffico correttamente, potresti aver bisogno di [aggiungere le rotte manualmente](https://discussions.apple.com/thread/2735376).

*Disinstalla tutte le versioni precedenti prima dell'aggiornamento.*

## POP VPN SSL (siti)

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


**Nota: disinstalla tutte le versioni precedenti del client prima di installare la nuova versione.**

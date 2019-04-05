---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connessione alla VPN SSL – MAC OSX 10x e superiore
{:#connect-ssl-vpn-mac-osx}

Installa l'ultima versione del client Mac MotionPro v1.1.7 dall'Apple Store. Assicurati di disinstallare eventuali versioni precedenti prima dell'aggiornamento.

Dopo aver installato il nuovo client, vai alla seguente directory e avvia la VPN utilizzando l'applicazione del terminale. 

`/usr/local/motionpro/`

Da lì, immetti il seguente comando per stabilire la connessione alla VPN SSL:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

Un elenco di endpoint VPN è disponibile [qui](https://www.softlayer.com/vpn-access).

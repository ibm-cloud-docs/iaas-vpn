---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Utilizza la VPN SSL

1. Naviga al link **SSL VPN Login** nel portale del cliente selezionando **Support > SSL VPN Login** dal menu di navigazione, quindi immetti le tue credenziali.
2. Il tunnel VPN SSL viene stabilito quando vedi una "A" nella tua barra delle attività.
3. Congratulazioni - sei ora in una VLAN privata.

## Ora sono collegato...cosa faccio?

1. Utilizza SSH o RDC (servizi del terminale) per collegarti all'indirizzo IP privato del tuo server (10.x.x.x) per la gestione del server.
2. Per utilizzare la console remota o riavviare le funzioni, collega la tua scheda IPMI 2.0 tramite il software SuperMicro - fai riferimento al [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) per le istruzioni di scaricamento.
3. Puoi associare un'unità al tuo server (Windows) o montarla sul tuo server (Red Hat).

## Suggerimenti e indicazioni 

1. I tuoi IP IPMI e privato sono numeri separati - non li far mischiare.
2. Non puoi utilizzare SSH o RDC per collegarti alla scheda IPMI, devi utilizzare il software.
3. I tuoi IP IPMI e privato si trovano nella tua sezione hardware in ogni **Server**.
4. La tua scheda IPMI "è in ascolto" nell'interfaccia dell'IP privato e reindirizza il traffico IPMI alla scheda IPMI.

**Avvertenza:**

Se disabiliti `eth0` (che è l'interfaccia di rete privata), perderai tutte le funzionalità IPMI incluso il monitoraggio, la console remota, il riavvio remoto e altro. Se vuoi bloccare l'accesso all'interfaccia privata, consulta il nostro elenco di indirizzi IP consentiti che puoi immettere nelle tabelle di IP o nel firewall del server.

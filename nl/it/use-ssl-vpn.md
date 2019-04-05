---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Utilizza la VPN SSL
{:#use-ssl-vpn}

1. Naviga al link **SSL VPN Login** nel portale del cliente selezionando **Support > SSL VPN Login** dal menu di navigazione, quindi immetti le tue credenziali.
2. Il tunnel VPN SSL viene stabilito quando vedi una "A" nella tua barra delle attività.
3. Congratulazioni - sei ora in una VLAN privata.

## Ora sono connesso... cosa faccio?
{:#now-im-connected-what-do-i-do}

1. Utilizza SSH o RDC (servizi del terminale) per connetterti all'indirizzo IP privato del tuo server (10.x.x.x) per la gestione del server.
2. Per utilizzare la console remota o riavviare le funzioni, connettiti alla tua scheda IPMI 2.0 tramite il software SuperMicro - fai riferimento al [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) per le istruzioni di scaricamento.
3. Puoi associare un'unità al tuo server (Windows) o montarla sul tuo server (Red Hat).

## Suggerimenti e indicazioni
{:#ssl-vpn-tips-tricks}

1. I tuoi IP IPMI e privato sono numeri separati - non li far mischiare.
2. Non puoi utilizzare SSH o RDC per connetterti alla scheda IPMI, devi utilizzare il software.
3. I tuoi IP IPMI e privato si trovano nella tua sezione hardware in ogni **Server**.
4. La tua scheda IPMI "è in ascolto" nell'interfaccia dell'IP privato e reindirizza il traffico IPMI alla scheda IPMI.

## Istruzioni IPMI specifiche per il prodotto
{:#product-specific-impi-instructions}

* Per ulteriori informazioni sull'utilizzo di IPMI su una condivisione CIFS, vedi [Mounting an ISO on a bare metal server](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-).
* Per ulteriori informazioni sull'utilizzo di IPMI con VMWare, vedi [Installing VMware vSphere ESXi via Remote Console and Virtual Media](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi).

* Per ulteriori informazioni sull'utilizzo di IPMI con l'hardware IBM POWER, vedi [Installing IPMItool](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm).

**Avvertenza:**

Se disabiliti `eth0` (che è l'interfaccia di rete privata), perderai tutte le funzionalità IPMI incluso il monitoraggio, la console remota, il riavvio remoto e altro. Se vuoi bloccare l'accesso all'interfaccia privata, consulta il nostro elenco di indirizzi IP consentiti che puoi immettere nelle tabelle di IP o nel firewall del server.

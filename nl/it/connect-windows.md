---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connessione alla VPN SSL - Windows 7 e superiore
{:#connect-ssl-vpn-windows7}

Per connetterti alla VPN SSL {{site.data.keyword.BluSoftlayer_notm}}, potresti aver bisogno di effettuare alcuni passi sul tuo computer per essere sicuro di poterti collegare.

**1. Disattiva User Access Control (UAC) nel pannello di controllo**

1. Passa a **Start -> Pannello di controllo -> Account utenti -> Modifica le impostazioni di controllo dell'account utente**
* **Deseleziona** la casella accanto a **Use User Account Control (UAC) per proteggere il tuo computer**.

**2. Abilita l'account amministratore**

1. Vai a **Start -> Pannello di controllo -> Strumenti di amministrazione -> Gestione computer -> Utenti e gruppi locali -> Utenti ->** 
* Fai clic con il tasto destro sull'utente **Amministratore** e seleziona **Proprietà** 
* Deseleziona a casella per **Account disabilitato**.

**3. Esegui Internet Explorer come amministratore prima di connetterti alla pagina VPN SSL**

1. Fai clic con il tasto destro sull'icona Internet Explorer e seleziona **Esegui come amministratore** dal menu.

Una volta completati i passi precedenti, dovresti essere in grado di accedere. 

## Accedi
{:#connect-windows-login}

1. Vai a [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) e accedi utilizzando i tuoi nome utente e password del portale. 
* Assicurati che il tuo utente [abbia l'accesso VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user).  
* Inoltre, assicurati di aver impostato una password VPN. Per far ciò, aggiorna la tua [User Profile Page](https://control.softlayer.com/account/user/profile) e compila la casella **VPN Password**.

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration d'un VPN PPTP pour Windows Vista

La connexion VPN PPTP permet une connexion à distance au réseau privé de {{site.data.keyword.BluSoftlayer_notm}} à partir d'un ordinateur de bureau ou d'un équipement dédié. La connexion au réseau privé via PPTP est disponible pour de multiples systèmes d'exploitation, dont Windows Vista. Les utilisateurs peuvent se connecter depuis tout centre de données {{site.data.keyword.BluSoftlayer_notm}} en entrant l'adresse de destination unique du centre de données lors de la configuration. Suivez les étapes ci-dessous pour configurer une connexion VPN PPTP sous Windows Vista. 

## Configuration d'une connexion VPN PPTP

1. Reportez-vous à la [page d'informations](http://windows.microsoft.com/en-US/windows-vista/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} de Microsoft pour atteindre l'écran permettant de configurer la connexion à distance. 

2. Entrez l'adresse de destination du centre de données souhaité dans la zone Adresse Internet. Reportez-vous au tableau ci-dessous pour les adresses appropriées des centres de données {{site.data.keyword.BluSoftlayer_notm}} actuels.

|Emplacement du centre de données|Adresse Internet du centre de données|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapour, SG|pptpvpn.sng01.softlayer.com|

3. Entrez un nom d'identification pour la connexion dans la zone de **nom de destination**.

**Remarque :** il est recommandé d'utiliser l'emplacement du centre de données comme nom de destination.

4. Entrez votre **nom d'utilisateur du Portail client** dans la zone Nom d'utilisateur. 

5. Entrez votre **mot de passe de Portail client** dans la zone Mot de passe.

6. Cliquez sur le bouton **Connecter**.

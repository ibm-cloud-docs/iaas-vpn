---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration d'un VPN PPTP pour Mac OS X 10.X

La connexion VPN PPTP permet une connexion à distance au réseau privé de {{site.data.keyword.BluSoftlayer_notm}} à partir d'un ordinateur de bureau ou d'un équipement dédié. La connexion au réseau privé via PPTP est disponible pour de multiples systèmes d'exploitation, dont Mac OS X. Les utilisateurs peuvent se connecter depuis tout centre de données {{site.data.keyword.BluSoftlayer_notm}} en entrant l'adresse de destination unique du centre de données lors de la configuration. Procédez comme suit pour configurer une connexion VPN PPTP sous Mac OS X. 

## Configuration d'une connexion VPN PPTP

* Sélectionnez **System Preferences** dans le menu déroulant **Apple**. 
* Cliquez sur l'icône de **réseau** dans la section Internet & Réseau. 
* Cliquez sur l'icône de **signe Plus** en bas du menu **Connexions**. Une boîte de dialogue en incrustation permettant de créer la connexion VPN s'affiche.
* Créez la connexion VPN comme suit :
  * Sélectionnez **VPN** dans la liste déroulante **Interface**. 
  * sélectionnez **PPTP** dans la liste déroulante **Type de VPN**. 
  * Entrez un **titre descriptif** pour la connexion dans la zone **Nom de service**. 
  * **Remarque :** il est recommandé d'insérer l'emplacement du centre de données dans le nom du service.
  * Cliquez sur le bouton **Créer**.
* Cliquez sur la connexion qui vient d'être créée dans le menu Connexions. 
* Entrez **l'adresse de destination** du centre de données souhaité dans la zone **Adresse du serveur**. Reportez-vous au tableau ci-dessous pour les adresses appropriées des centres de données {{site.data.keyword.BluSoftlayer_notm}} actuels.
* Entrez votre **nom d'utilisateur du Portail client** dans la zone **Nom de Compte**. 
* Renseignez les paramètres d'authentification. 
  * Cliquez sur le bouton **Paramètres d'authentification**. Une boîte de dialogue en incrustation invitant à l'authentification du VPN s’affiche. 
  * Entrez  votre **mot de passe VPN de client** dans la zone **Mot de passe**. 
  * Cliquez sur le bouton **OK**. 
* Mettez à jour les paramètres de trafic VPN. 
  * Cliquez sur le bouton **Avancé**. 
  * Vérifiez que la case **Send all traffic over VPN Connection** de la section Session n'est pas sélectionnée.
  * Cliquez sur le bouton **OK**. 
* Cochez la case **Show VPN Status in menu bar**. 
* Cliquez sur le bouton Appliquer. La connexion VPN peut maintenant être établie à tout moment à l'aide de l'élément VPN de la barre de menu. 

|Emplacement du centre de données|Adresse Internet du centre de données|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapour, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, HK|pptpvpn.hkg02.softlayer.com|
|Melbourne, AU|pptpvpn.mel01.softlayer.com|
|Londres, UK|pptpvpn.lon02.softlayer.com|
|Paris, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokyo, JP|pptpvpn.tok02.softlayer.com|

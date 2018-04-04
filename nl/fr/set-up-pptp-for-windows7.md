---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration d'un VPN PPTP pour Windows 7

La connexion VPN PPTP permet une connexion à distance au réseau privé de {{site.data.keyword.BluSoftlayer_notm}} à partir d'un ordinateur de bureau ou d'un équipement dédié. La connexion au réseau privé via PPTP est disponible pour de multiples systèmes d'exploitation, dont Windows 7. Les utilisateurs peuvent se connecter depuis tout centre de données {{site.data.keyword.BluSoftlayer_notm}} en entrant l'adresse de destination unique du centre de données lors de la configuration. Suivez les étapes ci-dessous pour configurer une connexion VPN PPTP sous Windows 7. 

## Configuration d'une connexion VPN PPTP

1. Reportez-vous à la [page d'informations](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} de Microsoft pour atteindre l'écran permettant de configurer la connexion à distance. 

2. Entrez l'adresse de destination du centre de données souhaité dans la zone Adresse Internet. Reportez-vous au tableau ci-dessous pour les adresses appropriées des centres de données IBM Cloud actuels.

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

3\. Entrez un nom d'identification pour la connexion dans la zone de **nom de destination**.

**Remarque :** il est recommandé d'utiliser l'emplacement du centre de données comme nom de destination.

4\. Entrez votre nom d'utilisateur pour le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) dans la zone **Nom d'utilisateur**.

5\. Entrez votre **mot de passe VPN** dans la zone **Mot de passe**.

6\. Cliquez sur le bouton **Connecter**.

7\. Maintenant, sur votre ordinateur, vous devez désactiver la passerelle distante pour pouvoir vous connecter à Internet et au VPN. 

8\. Cliquez sur **Démarrer**, puis sélectionnez **Panneau de configuration** -> **Centre Réseau et partage** -> **Modifier vos paramètres réseau**.

9\. Cliquez sur la connexion VPN PPTP avec le bouton droit de la souris, puis cliquez sur **Propriétés**.

10\. Décochez la case TCP/IPv6, puis cliquez sur TCP/IPv4 et sur Propriétés.

11\. Cliquez sur le bouton **Avancé**. 

12\. Décochez la case **Use Default Gateway on Remote Network**, puis cliquez sur **OK**.

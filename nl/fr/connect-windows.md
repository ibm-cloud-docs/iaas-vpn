---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connexion au VPN SSL - Windows 7 et versions ultérieures

Afin de vous connecter au VPN SSL de {{site.data.keyword.BluSoftlayer_notm}}, vous devrez peut-être effectuer quelques réglages sur votre ordinateur.

**1. Désactivez UAC (User Access Control) sur le panneau de configuration**

1. Accédez à **Démarrer -> Panneau de configuration -> Comptes d'utilisateurs -> Modifier les paramètres de contrôle de compte d’utilisateur**
* **Désactivez** la case **Use User Account Control (UAC) to help protect your computer**.

**2. Activez le compte administrateur**

1. Accédez à **Démarrer -> Panneau de configuration -> Outils d'administration -> Gestion de l'ordinateur -> Utilisateurs et groupes locaux -> Utilisateurs ->** 
* Cliquez avec le bouton droit de la souris sur l'utilisateur **Administrateur**, puis sélectionnez **Propriétés** 
* Décochez la case **Le compte est désactivé**.

**3. Exécutez Internet Explorer en tant qu'administrateur avant de vous connecter à la page VPN SSL**

1. Cliquez sur l'icône Internet Explorer avec le bouton droit de la souris, puis sélectionnez **Exécuter en tant qu'administrateur** dans le menu.

Une fois ces étapes terminées, vous devriez être en mesure de vous connecter. 

## Connexion

1. Accédez à [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) et connectez-vous à l'aide de vos nom d'utilisateur et mot de passe de portail. 
* Vérifiez que votre utilisateur [dispose d'un accès au VPN SSL](edit-users-vpn-access.html).  
* Vérifiez également qu'un mot de passe VPN a été défini. Pour ce faire, mettez à jour votre [page de profil utilisateur](https://control.softlayer.com/account/user/profile) et renseignez la zone **Mot de passe VPN**.

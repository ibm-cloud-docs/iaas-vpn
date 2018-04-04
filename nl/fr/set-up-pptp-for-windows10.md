---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration d'un VPN PPTP sous Windows 10

1. Ouvrez l'application **Paramètres** à partir du menu **Démarrer**, puis cliquez sur **Réseau et Internet**.

2. Sur la gauche du panneau **Réseau et Internet**, sélectionnez **VPN** et sur la page suivante, sélectionnez **Ajouter une connexion VPN**.

![Ajouter une connexion VPN](images/vpn1.png)

3. Sur la page qui suit, vous allez configurer vos connexions VPN PPTP. Les paramètres à configurer sont les suivants :

 * _Fournisseur VPN :_ Windows (intégré)
 * _Connexion :_ vous devez attribuer un nom à cette connexion, par exemple `MyPPTP`.
 * _Nom ou adresse du serveur :_ entrez le nom du serveur que vous voulez atteindre. (Par exemple, `pptpvpn.dal01.softlayer.com`)
 * _Type de VPN :_ sélectionnez PPTP (Point to Point Tunneling Protocol)
 *_ Type d’informations de connexion :_ sélectionnez Nom d'utilisateur et mot de passe
  * Saisissez ensuite votre nom d'utilisateur et votre mot de passe VPN
  * Vérifiez encore une fois toutes les valeurs sélectionnées, puis cliquez sur **Sauvegarder**

![Paramètres VPN](images/vpn2.png)

4. Une fois de retour sur la page VPN principale, cliquez sur la connexion `MyPPTP` précédemment créée pour vous connecter.

![PPTP Softlayer](images/vpn3.png)

5. Pour utiliser Internet tout en étant connecté, vous devez désactiver la passerelle distante, ce qui peut se faire via PowerShell.

 * Cliquez sur PowerShell avec le bouton droit de la souris pour l'ouvrir, puis sélectionnez **Exécuter en tant qu'administrateur**
 * Entrez les commandes suivantes :
 ```
`Get-VpnConnection`
`Set-VpnConnection -Name "MyPPTP" -SplitTunneling $True`
```

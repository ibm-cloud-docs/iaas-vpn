---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration d'un VPN IPSec

## Qu'est-ce qu'un VPN IPSec ?

IPSec est une suite de protocoles conçue pour authentifier et chiffrer l'intégralité du trafic IP entre deux emplacements, en utilisant un mode tunnel qui fournit un réseau de site à site chiffré. Cette suite permet de transmettre des données sécurisées via des réseaux qui autrement seraient considérés comme non sécurisés. Pour plus d'informations concernant IPSec, voir la [documentation de référence](external-reference.html).


L'accès VPN d'IBM Cloud permet aux utilisateurs de gérer à distance tous les serveurs en toute sécurité via le réseau privé d'IBM Cloud. Une connexion VPN de votre site vers le réseau privé permet une gestion externe et la récupération de serveurs via un tunnel VPN chiffré.  Avec l'accès au VPN, vous pouvez :

   -Etablir une connexion VPN au réseau privé via SSL, PPTP ou IPSEC
   -Accéder à votre serveur via son adresse IP 10.x.x.x privée via SSH ou RDP
   -Etablir une connexion à l'adresse IP IPMI de votre serveur à des fins de gestion ou de récupération de serveur supplémentaires.

Nous offrons à nos client le service IPSec pour la gestion de leurs environnements. Ce service n'est pas adapté aux charges de travail de production.


## Configuration d'une connexion IPSec

### Paramètres de négociation
![Paramètres de négociation](images/IPSec_VPN.png)

Vous devez connaître les informations suivantes concernant le site distant du VPN IPSec :
- Adresse IP statique du point d'accès VPN
- Clé pré-partagée (mot de passe)
- Algorithme de chiffrement (DES, 3DES, AES128, AES192, AES256)
- Authentification (MD5, SHA1, SHA256, pour phases 1&2)
- Groupe Diffie-Hellman (pour phases 1&2)
- Si la confidentialité de transmission parfaite (PFS) est utilisée
- Heure Keylife (pour phases 1 & 2) - **REMARQUE :** notre système mesure cette valeur en secondes. 

Une fois que vous disposez de ces informations, vous pouvez configurer les paramètres de négociation de base de la connexion VPN.

### Réseaux Protégés
![Réseaux Protégés](http://14bc7.http.dal05.cdn.softlayer.net/images/protected_networks.png)

Dans les propriétés de la connexion VPN, vous devez définir les réseaux sur le site distant du tunnel ainsi que les réseaux locaux pour le tunnel. Dans la section “Protected Customer (Remote) Subnet”, indiquez en notation CIDR l'espace d'adresse IP privé du site distant (non IBM) du tunnel IPSec.

<span style="text-decoration: underline">Par exemple :</span> si votre réseau sur le site distant du tunnel utilise un seul sous-réseau 10.0.0.0 avec un masque de réseau 255.255.255.0, entrez l'adresse IP 10.0.0.0 / CIDR 24 dans la section “Protected Customer (Remote) Subnet”.

### Conversion d'adresses réseau NAT (Network Address Translation)
![Conversion d'adresses réseau](http://14bc7.http.dal05.cdn.softlayer.net/images/nat.png)

Le VPN IPSec permet également de définir des adresses IP privées sur le réseau {{site.data.keyword.BluSoftlayer_notm}} afin d'acheminer le trafic vers des sous-réseaux distants à l'autre extrémité de la connexion VPN. Ainsi, vous pouvez acheminer le trafic Internet privé vers l'une de vos adresses IP internes d'une machine située derrière votre VPN, sans exposer le site distant à un accès Internet complet.  

### Conversion NAT/Sous-Réseaux NAT Statiques Affectés

Pour configurer une adresse IP de VPN distante avec une entrée NAT statique : 

 * Cliquez sur la flèche rouge pour afficher la liste des sous-réseaux dans la section **Sous-Réseaux NAT Statiques Affectés**. Toutes les adresses IP du sous-réseau sont affichées.  
 * Entrez l'adresse IP sur le site distant de la connexion VPN dans la colonne **IP Client** et entrez un nom pour le mappage dans la colonne **Nom**.  
 * Sélectionnez **Add/Modify Context Address Translations** et **Apply Configurations** pour sauvegarder et appliquer la configuration.
 
Cette procédure définit une conversion réseau un à un statique pour le trafic retour, qui est utilisée par vos hôte derrière le concentrateur VPN d'IBM Cloud pour communiquer avec les hôtes situés derrière l'homologue VPN distant. Par exemple, l'intégralité du trafic de l'adresse IP 10.1.255.92 sera convertie et acheminée vers l'adresse IP 192.168.10.15 du client. Ce réacheminement supprime le besoin d'entrées de routes supplémentaires sur le serveur IBM Cloud.

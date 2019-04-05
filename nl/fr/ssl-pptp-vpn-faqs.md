---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# Foire aux questions sur le VPN (réseau privé virtuel)
{:#vpn-faq}

## Qu'est-ce que le VPN IBM Cloud ?
{:#what-is-ibm-cloud-vpn}
{:faq}

Le VPN (réseau privé virtuel) IBM Cloud est conçu de manière à permettre aux utilisateurs de gérer à distance tous les serveurs en toute sécurité via l'accès au réseau privé IBM Cloud.  Une connexion VPN depuis votre emplacement vers le réseau privé permet la gestion externe et la récupération des serveurs via un tunnel VPN chiffré. Avec l'accès au VPN, vous pouvez :

* Etablir une connexion VPN au réseau privé à l'aide de SSL ou IPSEC
* Accéder à votre serveur via son adresse IP 10.x.x.x privée à l'aide de SSH ou RDP
* Etablir une connexion à l'adresse IP IPMI de votre serveur à des fins de récupération ou de gestion de serveur supplémentaires.


## Le VPN SSL exécute-t-il également des protocoles PPTP, IPSEC ou d'autres protocoles VPN ?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Actuellement, la passerelle VPN SSL utilise un plug-in VPN SSL basé sur un navigateur ou un client propriétaire pour la création des connexions. Nous continuerons d'apporter plus d'options de connectivité VPN vers le réseau privé. Le VPN SSL a été choisi pour sa facilité d'utilisation et sa compatibilité. PPTP est désormais obsolète. Pour plus d'informations, voir [Dépréciation du VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).



## Puis-je monter le serveur NAS/FTP depuis mon site distant sur la passerelle VPN SSL ?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

Non. Vous avez uniquement accès à votre VLAN privé et aux serveurs depuis la passerelle VPN SSL. Si vous souhaitez télécharger des données à partir de votre volume NAS/FTP, vous devez déplacer les données vers votre serveur, puis vers l'emplacement distant via le VPN.

Pour des raisons de sécurité, seuls les serveurs situés à l'intérieur du centre de données sont autorisés à accéder aux serveurs fournissant les services (DNS, Update, NAS, Lockbox).


## Quel fournisseur construit le VPN SSL et comment fonctionne-t-il ?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Notre passerelle VPN SSL est un produit de sécurité de Array Networks.  La passerelle elle-même exécute radius pour mettre à jour les utilisateurs et les mots de passe à partir de notre Portail client. Pour ajouter des utilisateurs et leur donner l'accès VPN SSL, créez un nouvel utilisateur à l'intérieur du portail client et activez les autorisations VPN SSL.


## Quelle est la différence entre un VPN SSL et un VPN PPTP ?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

Un **VPN SSL** permet à un utilisateur de créer un tunnel sécurisé du bureau à distance vers le réseau privé d'{{site.data.keyword.BluSoftlayer_notm}}. Il est compatible avec une grande variété de systèmes d'exploitation.

Un **VPN PPTP** permet de créer le même tunnel sécurisé, mais se connecte en utilisant un logiciel client spécialisé sur le bureau d'un utilisateur ou un équipement dédié. Toutefois, ceux-ci ont été dépréciés. Pour plus d'informations, voir [Dépréciation du VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Pourquoi ne puis-je pas ajouter d'utilisateurs supplémentaires pour le VPN PPTP ?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP est désormais obsolète. Pour plus d'informations, voir [Dépréciation du VPN PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).

## Quelles sont les catégories de statut de gestion de VPN d'utilisateur disponibles au sein du portail client ?
{:#what-are-available-categories-vpn-management}
{:faq}

Les catégories de statut client incluent celles pouvant être mises à jour par un utilisateur et celles qui peuvent s'afficher automatiquement. A savoir :

* **Actif** - l'utilisateur a accès au [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) et au VPN selon les droits définis par l'administrateur de compte. Ce statut peut être sélectionné manuellement et modifié à tout moment.
* **Désactivé** - l'utilisateur n'a accès à aucun droit ni abonnement sur le compte, y compris le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) et le VPN. Si ce statut a été défini par un autre utilisateur du compte, il peut être sélectionné manuellement et/ou modifié à tout moment.
* **VPN uniquement** - l'utilisateur peut uniquement accéder à la connectivité VPN et ne peut pas accéder au [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). Ce statut peut être sélectionné manuellement et modifié à tout moment.
* **Inactif** - l'utilisateur n'a pas accédé au [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) ni au VPN au cours des 60 derniers jours. Ce statut est généré par le système.
* **Annulation en attente** - un administrateur sur le compte a annulé cet utilisateur et l'annulation est en cours de traitement. Ce statut est généré par le système.

## Comment configurer le réseau VPN SSL ?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

Pour obtenir des instructions détaillées, voir [Connexion au VPN SSL - Windows 7 et versions ultérieures](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A propos du VPN
{:#about-iaas-vpn}

L'accès VPN vous permet de gérer à distance tous les serveurs et services associés à votre compte via le réseau privé d'IBM Cloud. Une connexion VPN depuis votre emplacement vers le réseau privé permet une **gestion externe et une récupération du serveur** via un tunnel VPN chiffré.

La communication à l'aide du réseau privé est intrinsèquement plus sécurisée. Elle vous offre la possibilité de limiter l'accès public tout en étant capable de gérer vos serveurs. Tout utilisateur sur votre compte peut avoir accès au VPN, lequel est disponible en connexion SSL. Les interactions VPN via le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) permettent de personnaliser l'accès VPN au niveau de l'utilisateur.

## Différentes manières d'utiliser le VPN SSL
{:#ways-to-use-iaas-vpn}

Cette passerelle sécurisée externe vous permet d'accéder à votre serveur sur le réseau privé. Utilisations courantes :

* Connexion à l'adresse IP privée de votre serveur (10.x.x.x) pour SSH ou RDC.
* Connexion à votre carte IPMI pour accès à/surveillance de la console distante.
* Montage d'unités sous Windows ou Red Hat à partir d'un PC situé au domicile ou au travail pour davantage de confort.
* Arrêt de l'interface publique sur les serveurs de bases de données et gestion sur le réseau privé.
* Arrêt de l'interface publique pendant la première configuration du serveur.
* Arrêt de l'interface publique pendant les mises à jour de sécurité critiques.
* Arrêt de l'interface publique en cas de une violation de sécurité et résolution du problème sur le réseau privé.

## Fonctions principales
{:#iaas-vpn-key-features}

 * Notre réseau privé vous offre un moyen gratuit pour communiquer avec les serveurs et pour les gérer. Le VPN est la passerelle vers ce réseau privé.
 * De nombreux points d'accès partout dans le monde autorisent l'accès et les interactions les meilleurs et les plus rapides possibles. IBM Cloud offre actuellement des points d'accès VPN dans un grand nombre de villes.
 * Rendez-vous sur http://www.softlayer.com/vpn-access pour la liste des points d'accès VPN au réseau privé d'{{site.data.keyword.BluSoftlayer_notm}}.

## Fonctionnement
{:#iaas-vpn-how-it-works}

Avec un accès VPN, utilisez SSL pour vous connecter au réseau privé et gérer votre serveur et vos services. 

## Connexions VPN SSL
{:#iaas-vpn-ssl-vpn-connections}

Le VPN SSL est une connexion à accès rapide qui vous relie à notre réseau privé directement à partir d'un navigateur. Le VPN SSL est compatible avec Windows XP ou une version ultérieure et avec ActiveX, Fedora, Ubuntu et Mac OSX. L'accès global à notre réseau privé est disponible à une adresse URL unique qui vous permet de choisir le point d'accès VPN le plus proche.

## Limite de sous-réseaux VPN SSL
{:#iaas-vpn-ssl-vpn-subnet-limit}

Le client VPN SSL a une limite fixe de 64 sous-réseaux, qu'il peut utiliser pour remplir sa table de routage. Si votre compte a plus de 64 sous-réseaux, veillez à modifier vos droits VPN SSL pour pouvoir utiliser l'affectation manuelle de sous-réseaux. Si vous ne le faites pas, certains sous-réseaux risquent d'être inaccessibles via le VPN SSL.

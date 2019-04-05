---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Dépréciation du VPN PPTP
{:#pptp-vpn-deprecation}

Le VPN PPTP est obsolète depuis le 12 juin 2018, et n'est plus proposé aux clients. Nous vous remercions pour l'intérêt que vous portez à ce service. Pour en savoir plus sur les solutions alternatives, lisez ce qui suit.

## Qu'est-ce qu'un VPN ?
{:#pptp-vpn-deprecation-what-is-vpn}
L'accès VPN permet aux utilisateurs de gérer à distance tous les serveurs en toute sécurité via le réseau privé d'IBM Cloud. Une connexion VPN depuis votre emplacement vers le réseau privé permet la gestion externe et la récupération des serveurs via un tunnel VPN chiffré. Avec l'accès au VPN, vous pouvez :

* Etablir une connexion VPN au réseau privé à l'aide de SSL, de **PPTP** ou d'IPSec
* Accéder sous SSH ou RDP à votre serveur en utilisant son adresse IP privée 10.x.x.x IP
* Vous connecter à l'adresse IP IPMI de votre serveur à des fins supplémentaires de gestion ou de récupération du serveur

## Obsolescence de PPTP
{:#pptp-deprecation-vpn}
L'utilité de PPTP a diminué au fur et à mesure que d'autres options de réseau privé virtuel sont devenues plus sécurisées et versatiles. {{site.data.keyword.BluSoftlayer_notm}} fournit plusieurs autres options plus sophistiquées, comme SSL ou IPSec, et qui assurent une meilleure protection que PPTP.

**Pour ces raisons, {{site.data.keyword.BluSoftlayer_notm}} n'offre plus PPTP depuis le 12 juin 2018.**
{:important}


## Foire Aux Questions
{:#pptp-vpn-deprecation-faq}

**Q : Pourquoi PPTP a-t-il été rendu obsolète ?**

**R :** Pour permettre une protection optimale, {{site.data.keyword.BluSoftlayer_notm}} a cessé d'utiliser PPTP. {{site.data.keyword.BluSoftlayer_notm}} s'est engagé à faire de la sécurité des données de ses clients et de la confidentialité de leurs informations une de ses priorités majeures. 

**Q : Quels autres types d'accès VPN sont-ils disponibles, à part PPTP ?**

**R :** {{site.data.keyword.BluSoftlayer_notm}} offre plusieurs options ne nécessitant qu'une configuration simple.
  1. Le VPN SSL est une connexion à accès rapide qui vous relie à notre réseau privé directement à partir d'un navigateur. Le VPN SSL est compatible avec Windows XP ou une version ultérieure et avec ActiveX, Fedora, Ubuntu et Mac OSX. L'accès global à notre réseau privé est disponible à une adresse URL unique qui vous permet de choisir le point d'accès VPN le plus proche. Reportez-vous à [Configuration d'une connexion VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) pour une initiation à cette option.
  2. IPSec est une suite de protocoles conçue pour l'authentification et le chiffrement de tout le trafic IP entre deux emplacements. Elle permet aux données fiables de circuler entre des réseaux qui autrement seraient considérés comme non sécurisés. Pour plus d'informations générales sur IPSec et pour commencer à utiliser ce service, reportez-vous à la rubrique [Configuration d'un VPN IPSec](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) et aux autres [documents de référence](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation). 

**Q : Que faire si mes pratiques métier nécessitent PPTP ?**

**R :** Plusieurs options sont disponibles si vos besoins métier nécessitent PPTP. **Les options envisageables ne sont pas toutes couvertes ici. Notez que les options suivantes requièrent une configuration complète des deux noeuds finaux. Le client est responsable de la configuration de ces options.**
  1. Dispositif de routeur virtuel. Le dispositif de routeur virtuel, également dénommé Vyatta, fait office de passerelle et de routeur pour votre environnement. Il contient des zones composées de sous-réseaux. Des règles de pare-feu sont définies entre les zones pour leur communication entre-elles. Pour celles n'ayant pas besoin de communiquer avec d'autres zones, aucune règle de pare-feu n'est requise puisque tous les paquets seront délaissés. Voir [Initiation au dispositif de routeur virtuel](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance) pour plus d'informations sur la mise en route de ce service. 
  2. Pare-feu FSA. Le dispositif de sécurité FortiGate (FSA) 10 Gbit/s est un pare-feu physique qui peut être configuré pour protéger le trafic sur plusieurs réseaux locaux virtuels (VLAN) tant pour les réseaux publics que privés. Dans le portail client, il est désigné par le terme “Pare-feu multi-VLAN”. Voir [Initiation à FSA 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) pour plus d'informations sur la mise en route de ce service. 
 
Les options précédentes ne sont qu'une partie des possibilités que vous pouvez explorer si PPTP est requis pour vos besoins métier, mais que ce service n'est plus fourni par {{site.data.keyword.BluSoftlayer_notm}}. Merci de votre confiance.
{:note}

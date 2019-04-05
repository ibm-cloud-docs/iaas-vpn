---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Utilisation du VPN SSL
{:#use-ssl-vpn}

1. Accédez au lien **Connexion VPN SSL** du portail client en sélectionnant **Support > Connexion VPN SSL** depuis le menu de navigation, puis entrez vos données d'identification.
2. Le tunnel VPN SSL est établi lorsque vous voyez un "A" dans la barre des tâches.
3. Félicitations - Vous vous trouvez maintenant dans votre VLAN privé.

## Maintenant que je suis connecté, que dois-je faire ?
{:#now-im-connected-what-do-i-do}

1. Utilisez SSH ou RDC (Services de terminal) pour vous connecter à l'adresse IP privée de votre serveur (10.x.x.x) pour la gestion du serveur.
2. Pour utiliser les fonctions de console distante ou de redémarrage à distance, connectez-vous à votre carte IPMI 2.0 via le logiciel SuperMicro - voir le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) pour les instructions de téléchargement.
3. Vous pouvez mapper un lecteur sur votre serveur (Windows) ou monter un lecteur sur votre serveur (Red Hat).

## Conseils et astuces
{:#ssl-vpn-tips-tricks}

1. Votre adresse IP privée et votre adresse IP IPMI ont un chiffre d'écart - ne les confondez pas.
2. Vous ne pouvez pas utiliser SSH ou RDC pour la carte IPMI, vous devez utiliser le logiciel.
3. Votre adresse IP privée et votre adresse IP IPMI figurent dans la section Matériel, sous chaque **Serveur**.
4. Votre carte IPMI "écoute" sur l'interface IP privée et réachemine le trafic IPMI vers la carte IPMI.

## Instructions spécifiques à IPMI
{:#product-specific-impi-instructions}

* Pour plus d'informations sur l'utilisation d'IPMI sur un partage CIFS, voir [Montage d'une image ISO sur un serveur bare metal](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-).
* Pour plus d'informations sur l'utilisation d'IPMI avec VMWare, voir [Installation de VMware vSphere ESXi via la console distante et le support virtuel](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi).

* Pour plus d'informations sur l'utilisation d'IPMI avec IBM POWER, voir [Installing IPMItool](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm).

**Avertissement :**

Si vous désactivez `eth0` (interface réseau privée), vous perdrez toutes les fonctionnalités IPMI, y compris la surveillance, la console distante, le redémarrage à distance, et bien plus. Si vous voulez bloquer l'accès à l'interface privée, consultez notre liste des adresses IP autorisées à placer dans vos tables IP ou le pare-feu du serveur.

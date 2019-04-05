---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Linux Fedora, SSL VPN connections Windows, backend IP address

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configuration de connexions VPN SSL
{:#setup-ssl-vpn-connections}

Windows, Linux Fedora et Linux nécessitent des instructions de connexion personnalisées, indiquées dans ce document. Exemples d'utilisation d'une connexion VPN SSL :

* Bureau distant vers l'adresse IP de votre serveur de back end (10.4.X.X) pour l'administration de vos serveurs Windows 2003.
* SSH vers l'adresse IP de votre serveur de back end (10.4.X.X) pour l'administration de vos serveurs UNIX.
* Utilisation d'un client IPMI pour contrôler votre serveur via l'adresse IPMI de back end (10.4.X.X). Vous pouvez télécharger l'outil client IPMI une fois connecté en accédant à http://downloads.softlayer.local/ipmi/ (Vous devez être connecté au VPN privé SoftLayer).
  * **Remarque :** IPMIView exige que Java soit installé.  http://www.sun.com/java/
* Test de votre site Web sur les IP de back end avant de les rendre opérationnelles sur vos adresses IP publiques.
* Transfert de fichiers de données sécurisées entre votre ou vos serveurs et votre domicile/bureau.
* Sauvegarde des fichiers de configuration de votre ou vos serveurs sur le poste de votre domicile ou de votre bureau.
* Connexion sécurisée à notre [portail Web](http://control.softlayer.com/).

## Windows (Internet Explorer)
{:#setup-ssl-vpn-connections-windows}

1. Ouvrez Internet Explorer et accédez à `http://www.softlayer.com/vpn-access`.
* Une fois que vous avez saisi votre nom d'utilisateur et votre mot de passe, vous êtes invité à installer un plug-in ActiveX. Vous devez installer ce plug-in pour pouvoir vous connecter à votre réseau de back end. 
* Vous devez également disposer des droits administrateur sur votre poste de travail pour installer le plug-in ActiveX. Si vous ne disposez pas de droits d'installation pour le plug-in, demandez à votre administrateur système local de l'installer pour vous. 
* Une fois le plug-in ActiveX installé, un connecteur de réseau Array SSL VPN lance et établit une connexion au dispositif VPN. En cas de succès, un '**A**' rouge s'affiche dans la barre des tâches. Vous pouvez cliquer sur ce '**A**' à tout moment pour afficher le statut de votre connexion VPN SSL, l'adresse IP attribuée, les serveurs DNS attribués, les routes de réseau et le temps de connexion. 
* Vous pouvez à tout moment réduire votre session de navigateur et continuer à utiliser d'autres applications de façon sécurisée sur le réseau privé. 
* Lorsque vous avez terminé, déconnectez-vous en cliquant sur le bouton de déconnexion à droite ou en fermant simplement la fenêtre.

## Linux Fedora 
{:#setup-ssl-vpn-connections-linux}

Firefox ne prend plus en charge les plug-in NPAPI (applets Java). Utilisez un autre navigateur pour effectuer ces étapes.
{:note}

Il est recommandé d'exécuter toutes les commandes en tant que root. (`setuid root`)

1. Téléchargez Java depuis `http://java.com/en/download/manual.jsp`. Il s'agit d'un fichier auto-extractible.
* Fermez votre navigateur.
* Déplacez le fichier jusqu'à l'emplacement où vous voulez installer Java (en général `/usr/local`)
* Rendez le fichier exécutable avec la commande `chmod +x jre-6u1-linux-i586.bin`
* Lancez le programme d'installation avec la commande `./jre-6u1-linux-i586.bin`
* Acceptez les conditions et installez.
* Une fois l'installation terminée, vous devez créer une liaison symbolique (symlink).

## Exemple pour Linux
{:#setup-ssl-vpn-connections-linux-example}

1. Ouvrez votre navigateur et accédez à `http://www.softlayer.com/vpn-access`.
* Connectez-vous avec votre nom d'utilisateur et votre mot de passe de portail client.
* Une fois connecté, cliquez sur l'onglet **Réseau**.
* Vous devriez voir un bouton de connexion/installation. Cliquez dessus. Vous êtes alors invité à installer un composant Java.
* Acceptez d'installer le composant à l'emplacement pas défaut, que vous devrez peut-être créer manuellement. (`/usr/local/array_vpn`)
* Une fois le composant installé, une fenêtre indiquant que vous êtes connecté doit s'afficher.
* Cette fenêtre doit rester ouverte pour utiliser le tunnel VPN, mais vous pouvez la réduire.
* Pour tester la connexion, envoyez une commande ping à l'adresse 10.0.80.11 ou à l'adresse privée de votre serveur. Si vous obtenez une réponse, la connexion a réussi.
* Lorsque vous avez terminé, cliquez sur le bouton de déconnexion de l'onglet Réseau ou fermez simplement toutes les fenêtres de votre navigateur.

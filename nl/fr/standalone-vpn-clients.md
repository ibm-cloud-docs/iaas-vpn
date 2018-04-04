---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Clients VPN autonomes - Windows, Linux et Mac OS X

## Client autonome Windows

Windows (8/7/Vista/XP) 32 bits :  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) 64 bits :  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. Téléchargez l'un des fichiers répertoriés ci-dessous selon votre système d'exploitation.
* Exécutez MotionProSetup pour installer le logiciel.
* Exécutez MotionPro et, à l'ouverture de l'écran, sélectionnez **Profil -> Ajouter**.
* Créez un profil auquel vous attribuez un nom de site, en choisissant un nom d'hôte dans la liste des sites VPN SSL (ci-dessous). Ensuite, entrez vos nom d'utilisateur et mot de passe VPN, puis cliquez sur **Sauvegarder**.
* Enfin, cliquez deux fois sur le profil que vous venez de créer pour vous connecter au VPN.

**Remarques**
 * 'Site' peut être un nom de domaine ou une adresse IP.
 * En cas de problème, désinstallez tous les programmes Array via le panneau de configuration Windows, redémarrez, puis reconnectez-vous.
 * Ne fonctionne pas sous Windows 8 RT.

## Client autonome Linux 

CentOS 64 bits : https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat 32 bits : https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat 64 bits : https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu 32 bits : https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu 64 bits : https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. Rendez le fichier exécutable : `chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* Exécutez le script :  `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh.`
* Syntaxe :  `./MotionPro --host [site] --user [nom d'utilisateur] --passwd [mot de passe]`
* Pour l'arrêter :  `[control-c]`

**Notes : **  
 * Pour démarrer le client MotionPro, vous devez entrer au moins le `nom d'hôte` et le `nom d'utilisateur` comme arguments.
 * 'Site' peut être un nom de domaine ou une adresse IP.

## Client autonome Mac OS X 10.10

Procédure pour client VPN SSL Motion Pro Plus sous MacOS StandAlone Array :

1. Installez le client "Motion Pro Plus" depuis l'Apple store.
* Recherchez le client Pro Plus dans le dossier Applications et ouvrez l'application.
* Cliquez sur 'Profil', puis sur 'Ajouter'.
* Renseignez le nom de site, l'hôte et le nom d'utilisateur, puis cliquez sur OK.
* Cliquez sur VPN en haut à gauche, puis connectez-vous.

Exemple :

![Figure 1](images/snip20170425_1.png)

Si le tunnel n'achemine pas correctement le trafic, vous devrez peut-être [ajouter des routes manuellement](https://discussions.apple.com/thread/2735376).

*Avant de mettre à jour, désinstallez toutes les versions précédentes.*

## POP SSL VPN (sites)

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


**Important : veillez à désinstaller toutes les versions précédentes du client avant d'installer la nouvelle version.**

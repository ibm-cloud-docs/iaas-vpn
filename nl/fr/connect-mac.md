---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Connexion au VPN SSL – MAC OSX 10x et versions ultérieures
{:#connect-ssl-vpn-mac-osx}

Installez la dernière version du client Mac MotionPro v1.1.7 à partir de l'Apple Store. Assurez-vous de désinstaller toutes les versions précédentes avant de procéder à la mise à jour.

Après avoir installé le nouveau client, accédez au répertoire suivant et lancez le VPN à l'aide de l'application Terminal. 

`/usr/local/motionpro/`

Depuis ce répertoire, exécutez la commande ci-dessous pour vous connecter au VPN SSL :

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

La liste des noeuds finaux VPN est accessible [ici](https://www.softlayer.com/vpn-access).

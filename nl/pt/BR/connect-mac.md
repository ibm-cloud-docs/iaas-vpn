---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Conectar-se à VPN SSL – MAC OSX 10x e superior
{:#connect-ssl-vpn-mac-osx}

Instale a versão mais recente do cliente Mac MotionPro v1.1.7 na Apple Store. Certifique-se de desinstalar qualquer versão anterior antes de atualizar.

Depois de instalar o novo cliente, acesse o diretório a seguir e ative a VPN usando o aplicativo Terminal. 

`/usr/local/motionpro/`

Desse local, execute o comando a seguir para ser conectado à VPN SSL:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

Uma lista de terminais de VPN pode ser localizada [aqui](https://www.softlayer.com/vpn-access).

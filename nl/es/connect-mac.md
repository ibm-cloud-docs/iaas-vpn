---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN , MAC OSX 10x

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Conectarse a la VPN con SSL - MAC OSX 10x posterior
{:#connect-ssl-vpn-mac-osx}

Instale la última versión del cliente Mac MotionPro v1.1.7 desde Apple Store. Asegúrese de desinstalar las versiones anteriores antes de actualizar.

Tras instalar el nuevo cliente, vaya al directorio siguiente e inicie la VPN mediante la aplicación Terminal. 

`/usr/local/motionpro/`

Desde allí, ejecute el siguiente mandato para conectarse a la VPN con SSL:

`./vpn_cmdline -h vpn.wdc04.softlayer.com -u username -p password`

Puede obtener una lista de puntos finales de VPN [aquí](https://www.softlayer.com/vpn-access).

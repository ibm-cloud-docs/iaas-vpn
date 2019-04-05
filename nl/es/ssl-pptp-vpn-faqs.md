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

# Preguntas frecuentes de la VPN
{:#vpn-faq}

## ¿Qué es la VPN de IBM Cloud?
{:#what-is-ibm-cloud-vpn}
{:faq}

El acceso VPN de IBM Cloud está diseñado para permitir a los usuarios gestionar de manera remota y segura todos los servidores en la red privada de IBM Cloud.  Una conexión VPN desde su ubicación a la red privada permite la gestión fuera de banda y el rescate de servidor a través de un túnel VPN cifrado. Con el acceso VPN, puede:

* Establecer una conexión VPN a la red privada utilizando SSL o IPSEC.
* Acceder al servidor mediante la dirección de IP 10.x.x.x privada utilizando SSH o RDP.
* Conectarse a la dirección IP de IPMI del servidor para otras tareas de rescate y gestión de servidores.


## ¿La VPN con SSL también lleva a cabo los protocolos PPTP, IPSEC u otros protocolos VPN?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Actualmente, la pasarela de VPN con SSL utiliza un conector de VPN con SSL basado en navegador o un cliente de propietario para establecer las conexiones. Seguiremos introduciendo más opciones de conectividad VPN a la red privada. Se optó por la VPN con SSL por su facilidad de uso y compatibilidad. PPTP está en desuso. Consulte [VPN con PPTP en desuso](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obtener más información.



## ¿Puedo montar el servidor NAS/FTP desde mi ubicación remota en la pasarela VPN con SSL?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

No...solo tiene acceso a la VLAN privada y a los servidores desde la pasarela de VPN con SSL. Si desea descargar datos del volumen NAS/FTP, debe transferir los datos al servidor y de ahí, a través de VPN, a la ubicación remota.

Por motivos de seguridad, el acceso a los servidores que proporcionan servicios (DNS, actualización, NAS, caja de seguridad) solo está permitido para los servidores ubicados en el centro de datos.


## ¿Qué proveedor crea la VPN con SSL y cómo funciona?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Nuestra pasarela de VPN con SSL es un producto de seguridad de Array Networks.  La pasarela ejecuta el servicio de usuarios de autenticación para actualizar los usuarios y contraseñas desde nuestro Portal de clientes. Si desea añadir usuarios y concederles acceso a la VPN con SSL, cree un usuario nuevo en el portal de clientes y habilite los permisos de VPN con SSL.


## ¿Cuál es la diferencia entre la VPN con SSL y PPTP?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

La **VPN con SSL** le permite a un usuario crear un túnel seguro desde el escritorio remoto a la red privada de {{site.data.keyword.BluSoftlayer_notm}}. Es compatible con varios sistemas operativos.

La **VPN con PPTP** permite crear el mismo túnel seguro, pero este se conecta mediante un cliente de software especializado en el dispositivo dedicado o de escritorio del usuario. Sin embargo, PPTP está en desuso. Consulte [VPN con PPTP en desuso](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obtener más información.

## ¿Por qué no puedo añadir usuarios adicionales en la VPN con PPTP?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

PPTP está en desuso. Consulte [VPN con PPTP en desuso](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obtener más información.

## ¿Cuáles son las categorías disponibles para el estado de gestión de la VPN de un usuario en el Portal de clientes?
{:#what-are-available-categories-vpn-management}
{:faq}

Entre las categorías de estado del cliente se incluyen aquellas que los usuarios pueden actualizar y las que pueden aparecer automáticamente. Entre ellas se encuentran las siguientes:

* **Activo** - El usuario tiene acceso al [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y a las VPN basadas en los permisos establecidos por el administrador de la cuenta. Este estado se puede seleccionar o modificar de forma manual en cualquier momento.
* **Inhabilitado** - El usuario no tiene acceso a ningún permiso o suscripción a la cuenta, incluidos el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y la VPN. Si otro usuario de la cuenta lo establece en inhabilitado, el estado se puede seleccionar de forma manual y se puede modificar en cualquier momento.
* **Solo VPN** - El usuario solo tiene acceso a la conectividad VPN y es posible que no acceda al [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Este estado se puede seleccionar o modificar de forma manual en cualquier momento.
* **Inactivo** - El usuario no ha utilizado el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) o la VPN en los últimos 60 días. Este es un estado generado por el sistema.
* **cancel_pending** - Un administrador de la cuenta ha cancelado el usuario y la cancelación se está procesando. Este estado lo genera el sistema.

## ¿Cómo se configura SSL VPN?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

Para obtener instrucciones detalladas, consulte [Conectarse a la VPN con SSL - Windows 7 y posterior](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes de la VPN

## ¿Qué es la VPN de IBM Cloud?

El acceso VPN de IBM Cloud está diseñado para permitir a los usuarios gestionar de manera remota y segura todos los servidores en la red privada de IBM Cloud.  Una conexión VPN desde su ubicación a la red privada permite la gestión fuera de banda y el rescate de servidor a través de un túnel VPN cifrado. Con el acceso VPN, puede:

* Establecer una conexión VPN a la red privada utilizando SSL, PPTP o IPSEC
* Acceder al servidor mediante la dirección de IP 10.x.x.x privada utilizando SSH o RDP
* Conectarse a la dirección IP de IPMI del servidor para otras tareas de rescate y gestión de servidores.


## ¿La VPN con SSL también lleva a cabo los protocolos PPTP, IPSEC u otros protocolos VPN?

Actualmente, la pasarela de VPN con SSL utiliza un conector de VPN con SSL basado en navegador o un cliente de propietario para establecer las conexiones. Seguiremos introduciendo más opciones de conectividad VPN a la red privada. Se optó por la VPN con SSL por su facilidad de uso y compatibilidad.


<a name="152"></a>
## ¿Puedo montar el servidor NAS/FTP desde mi ubicación remota en la pasarela VPN con SSL?

No...solo tiene acceso a la VLAN privada y a los servidores desde la pasarela de VPN con SSL. Si desea descargar datos del volumen NAS/FTP, debe transferir los datos al servidor y de ahí, a través de VPN, a la ubicación remota.

Por motivos de seguridad, el acceso a los servidores que proporcionan servicios (DNS, actualización, NAS, caja de seguridad) solo está permitido para los servidores ubicados en el centro de datos.

<a name="175"></a>
## ¿Qué proveedor crea la VPN con SSL y cómo funciona?

Nuestra pasarela de VPN con SSL es un producto de seguridad de Array Networks.  La pasarela ejecuta el servicio de usuarios de autenticación para actualizar los usuarios y contraseñas desde nuestro Portal del cliente. Si desea añadir usuarios y concederles acceso a la VPN con SSL, cree un usuario nuevo en el portal y habilite los permisos de VPN con SSL.

<a name="276"></a>
## ¿Cuál es la diferencia entre la VPN con SSL y PPTP?

La **VPN con SSL** le permite a un usuario crear un túnel seguro desde el escritorio remoto a la red privada de {{site.data.keyword.BluSoftlayer_notm}}. Es compatible con varios sistemas operativos.

La **VPN con PPTP** permite crear el mismo túnel seguro, pero este se conecta mediante un cliente de software especializado en el dispositivo dedicado o de escritorio del usuario. La VPN con PPTP es una buena solución para los usuarios que no pueden utilizar una conexión SSL.

## Cuando me conecto a la VPN con PPTP, aparece el mensaje "Error 691: Se ha denegado el acceso porque el nombre de usuario o contraseña no son válidos". ¿Cómo se puede solucionar este problema?

Todos los usuarios tienen la capacidad de conectarse a la VPN con PPTP, pero deben tener permiso para iniciar sesión mediante el Portal del cliente.  Los permisos de la VPN con PPTP se verifican y actualizan de forma fácil y rápida.  Consulte [Activar o desactivar el acceso a VPN con PPTP](activate-a-user.html) para obtener más información.

## ¿Por qué no puedo añadir usuarios adicionales en la VPN con PPTP?

La VPN con PPTP está disponible en todas las cuentas, pero al principio está configurada para habilitar el acceso a un usuario a la vez. Para solicitar la habilitación de una cuenta y obtener protocolos PPTP ilimitados sin costes adicionales, cree una incidencia mediante el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) con la información siguiente junto con los detalles adicionales necesarios:

* Asunto: Solicitud de VPN con PPTP
* Texto: Actualmente el acceso con PPTP está limitado a un usuario a la vez. Habilite el acceso a VPN con PPTP ilimitado para mi cuenta.

Un miembro del equipo de soporte de IBM actualizará la cuenta para permitir el acceso PPTP ilimitado que está disponible sin cargos adicionales. La incidencia se actualizará si es necesaria cualquier información adicional.

## ¿Cuáles son las categorías disponibles para el estado de gestión de la VPN de un usuario en el Portal del cliente?

Entre las categorías de estado del cliente se incluyen aquellas que los usuarios pueden actualizar y las que pueden aparecer automáticamente. Entre ellas se encuentran las siguientes:

* **Activo** - El usuario tiene acceso al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y a las VPN basadas en los permisos establecidos por el administrador de la cuenta. Este estado se puede seleccionar o modificar de forma manual en cualquier momento.
* **Inhabilitado** - El usuario no tiene acceso a ningún permiso o suscripción a la cuenta, incluidos el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y la VPN. Si otro usuario de la cuenta lo establece en inhabilitado, el estado se puede seleccionar de forma manual y se puede modificar en cualquier momento.
* **Solo VPN** - El usuario solo tiene acceso a la conectividad VPN y es posible que no acceda al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Este estado se puede seleccionar o modificar de forma manual en cualquier momento.
* **Inactivo** - El usuario no ha utilizado el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) o la VPN en los últimos 60 días. Este es un estado generado por el sistema.
* **cancel_pending** - Un administrador de la cuenta ha cancelado el usuario y la cancelación se está procesando. Este estado lo genera el sistema.

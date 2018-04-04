---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes sobre la VPN con PPTP

## ¿Por qué no puedo añadir usuarios adicionales en la VPN con PPTP?

La VPN con PPTP está disponible en todas las cuentas, pero al principio está configurada para habilitar el acceso a un usuario a la vez. Para solicitar la habilitación de una cuenta y obtener protocolos PPTP ilimitados sin costes adicionales, cree una incidencia mediante el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) con la información siguiente junto con los detalles adicionales necesarios:

* Asunto: Solicitud de VPN con PPTP
* Texto: Actualmente el acceso con PPTP está limitado a un usuario a la vez. Habilite el acceso a VPN con PPTP ilimitado para mi cuenta.

Un miembro del equipo de soporte de IBM actualizará la cuenta para permitir el acceso PPTP ilimitado que está disponible sin cargos adicionales. La incidencia se actualizará si es necesaria cualquier información adicional.

## ¿Cuáles son las categorías disponibles del estado de un usuario en el Portal del cliente?

Entre las categorías de estado del cliente se incluyen aquellas que los usuarios pueden actualizar y las que pueden aparecer automáticamente. Entre ellas se encuentran las siguientes:

* **Activo** - El usuario tiene acceso al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y a las VPN basadas en los permisos establecidos por el administrador de la cuenta. Este estado se puede seleccionar manualmente y se puede modificar en cualquier momento.
* **Inhabilitado** - El usuario no tiene acceso a ningún permiso o suscripción a la cuenta, incluidos el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) y la VPN. Si otro usuario de la cuenta lo establece en inhabilitado, el estado se puede seleccionar de forma manual y se puede modificar en cualquier momento.
* **Solo VPN** - El usuario solo tiene acceso a la conectividad VPN y es posible que no acceda al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Este estado se puede seleccionar manualmente y se puede modificar en cualquier momento.
* **Inactivo** - El usuario no ha utilizado el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) o la VPN en los últimos 60 días. Este es un estado generado por el sistema.
* **cancel_pending** - Un administrador de la cuenta ha cancelado el usuario y la cancelación se está procesando. Este es un estado generado por el sistema.

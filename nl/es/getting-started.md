---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Iniciación a la red privada virtual (VPN)

## ¿Qué es la VPN de IBM Cloud?

El acceso VPN permite a los usuarios gestionar todos los servidores de forma remota y segura en la red privada de IBM Cloud. Una conexión VPN desde su ubicación a la red privada permite transferencias de archivos ilimitadas, la gestión fuera de banda y el rescate de servidor a través de un túnel VPN cifrado. Con el acceso VPN, puede:

* Establecer una conexión VPN a la red privada mediante SSL, PPTP o IPSEC
* Acceder al servidor con la dirección IP 10.x.x.x privada mediante SSH o RDP
* Conectarse a la dirección IP de IPMI del servidor para otras tareas de rescate y gestión de servidores.

Algunos servicios requieren acceso mediante la red privada, y la VPN es un método que permite el acceso de red privada. Conviene utilizar una VPN cuando necesite iniciar sesión en la red privada, realizar su trabajo y luego cerrar sesión. Por ejemplo, este acceso suele ser necesario para obtener el KVM del servidor.

Se puede proporcionar acceso VPN a cada cuenta de usuario, y puede limitarse en relación con las subredes a las que necesita acceso. Debe tener el acceso VPN habilitado y debe crear una contraseña de VPN para poder iniciar sesión en la VPN.

## Habilitar el acceso VPN de cada usuario

Para empezar, deberá habilitar el acceso VPN en las cuentas que lo necesiten. Al principio, todas las cuentas tienen el acceso VPN **inhabilitado**, incluida la cuenta maestra de su equipo. Para habilitar el acceso VPN, siga estos pasos:

1. Vaya a **Cuenta -> Acceso VPN** en el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
* Encontrará una fila para cada usuario de VPN posible y un enlace en la columna **Acceso VPN**.
* En el enlace se leerá "Ninguno" si el usuario todavía no tiene el acceso VPN habilitado.
* Si en el enlace de acceso VPN del usuario se lee **SSL, PPTP, o SSL y PPTP**, eso significa que el usuario ya ha activado el acceso VPN.

![Tabla de acceso VPN del portal de Softlayer](images/vpnaccess01.png)

1. Para habilitar o cambiar los tipos de acceso VPN permitidos de un usuario específico, pulse en el enlace de la columna **Acceso VPN**.
* En la página siguiente podrá habilitar el tipo de acceso VPN adecuado para cada usuario.  
* De forma predeterminada, solo un usuario puede tener acceso VPN con PPTP. Si la cuenta requiere más de un usuario de VPN con PPTP, póngase en contacto con nuestro equipo de soporte mediante el chat en directo, el sistema de incidencias o por teléfono para habilitar los usuarios de VPN con PPTP sin coste adicional.

![Asignar el tipo de acceso VPN a un usuario](images/vpntype01.png)

## Establecer la contraseña de VPN

El siguiente paso es crear una contraseña de VPN. Cada usuario puede crear y actualizar la contraseña de VPN en el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Para ello, seleccione su nombre en la parte superior derecha, que le llevará a la página **Editar perfil**. También puede seleccionar **Cuenta -> Usuarios** y, a continuación, seleccionar su nombre de usuario.

      Nota: En el enlace se lee "Usuario maestro". En el enlace los subusuarios verán su nombre.

En la página **Editar perfil de usuario**, desplácese hacia abajo e inicialice o actualice la contraseña de VPN.

![Editar los campos de contraseña de VPN del perfil](images/vpnpasswordfields.png)

## Iniciar sesión en la VPN

Ahora que se ha establecido el acceso VPN, puede iniciar sesión.

1. Para iniciar sesión en la VPN con SSL, visite [vpn.softlayer.com](https://vpn.softlayer.com/) y seleccione cualquiera de los puntos de inicio. Puede utilizar cualquier punto de acceso VPN, y se le proporcionan los mismos permisos de acceso a la red privada en todos los centros de datos.
* Si tiene problemas iniciando sesión en una ubicación, inténtelo en otra.
* De forma alternativa, puede iniciar sesión utilizando un cliente VPN con SSL autónomo.
* Podrá utilizar las utilidades del sistema operativo estándar para iniciar sesión en la VPN con PPTP.

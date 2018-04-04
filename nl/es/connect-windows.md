---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Conectarse a la VPN con SSL - Windows 7 y posterior

Para conectarse a la VPN con SSL de {{site.data.keyword.BluSoftlayer_notm}}, es posible que tenga que realizar los siguientes pasos en el sistema para garantizar la capacidad de conexión.

**1. Desactive el control de cuentas de usuario (UAC) en el panel de control**

1. Vaya a **Inicio -> Panel de control -> Cuentas de usuario -> Cambiar los valores del control de cuentas de usuario**
* **Desmarque** el recuadro junto a **Utilizar Control de cuentas de usuario (UAC) para ayudar a proteger el sistema**.

**2. Habilite la cuenta de administrador**

1. Vaya a **Inicio -> Panel de control -> Herramientas administrativas -> Gestión de sistemas -> Usuarios y grupos locales -> Usuarios ->** 
* Pulse con el botón derecho en el usuario **Administrador** y seleccione **Propiedades** 
* Desmarque el recuadro **La cuenta está inhabilitada**.

**3. Ejecute Internet Explorer como administrador antes de conectarse a la página de VPN con SSL.**

1. Pulse con el botón derecho el icono de Internet Explorer y seleccione **Ejecutar como administrador** desde el menú.

Cuando haya completado los pasos anteriores, debería poder iniciar sesión. 

## Iniciar sesión

1. Vaya a [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) e inicie sesión utilizando el nombre de usuario y la contraseña del portal. 
* Asegúrese de que el usuario [tiene acceso VPN con SSL](edit-users-vpn-access.html).  
* Asegúrese también de que ha establecido una contraseña de VPN. Para ello, actualice la [Página de perfil de usuario](https://control.softlayer.com/account/user/profile) y rellene el recuadro que dice **Contraseña de VPN**.

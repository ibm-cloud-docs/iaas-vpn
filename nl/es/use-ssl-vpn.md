---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Utilizar la VPN con SSL

1. Vaya al enlace **Inicio de sesión de la VPN con SSL** en el Portal del cliente seleccionando **Soporte > Inicio de sesión de la VPN con SSL** desde el menú de navegación y, a continuación, especifique las credenciales.
2. El túnel VPN con SSL se establece cuando visualiza la "A" en la barra de tareas.
3. Enhorabuena, ya se encuentra en su VLAN privada.

## Ahora que estoy conectado... ¿qué hago?

1. Utilice SSH o RDC (servicios de terminal) para conectarse a la dirección IP privada de su servidor (10.x.x.x) para la gestión del servidor.
2. Para utilizar la consola remota o las funciones de rearranque, conéctese a la tarjeta IPMI 2.0 mediante el software SuperMicro. Consulte el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) para obtener las instrucciones de descarga.
3. Puede correlacionar una unidad al servidor (Windows) o montar una unidad en el servidor (Red Hat).

## Sugerencias y consejos

1. Hay un dígito de diferencia entre la IP IPMI y la IP privada. No las mezcle.
2. No puede utilizar SSH o RDC para conectarse a la tarjeta IPMI; debe utilizar el software.
3. La IP IPMI y la IP privada se encuentran en la sección de hardware en cada **servidor**.
4. La tarjeta IPMI "escucha" la interfaz de IP privada y redirecciona el tráfico de IPMI a la tarjeta IPMI.

**Aviso:
**

Si inhabilita `eth0` (que es la interfaz de red privada), perderá todas las funcionalidades de IPMI, incluida la supervisión, la consola remota, el rearranque remoto, etc. Si desea bloquear el acceso a la interfaz privada, consulte la lista de direcciones IP permitidas que puede especificar en las tablas de IP o el cortafuegos del servidor.

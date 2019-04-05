---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Utilizar la VPN con SSL
{:#use-ssl-vpn}

1. Vaya al enlace **Inicio de sesión de la VPN con SSL** en el Portal de clientes seleccionando **Soporte > Inicio de sesión de la VPN con SSL** desde el menú de navegación y, a continuación, especifique las credenciales.
2. El túnel VPN con SSL se establece cuando visualiza la "A" en la barra de tareas.
3. Enhorabuena, ya se encuentra en su VLAN privada.

## Ahora que estoy conectado... ¿qué hago?
{:#now-im-connected-what-do-i-do}

1. Utilice SSH o RDC (servicios de terminal) para conectarse a la dirección IP privada de su servidor (10.x.x.x) para la gestión del servidor.
2. Para utilizar la consola remota o las funciones de rearranque, conéctese a la tarjeta IPMI 2.0 mediante el software SuperMicro. Consulte el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) para obtener las instrucciones de descarga.
3. Puede correlacionar una unidad al servidor (Windows) o montar una unidad en el servidor (Red Hat).

## Sugerencias y consejos
{:#ssl-vpn-tips-tricks}

1. Hay un dígito de diferencia entre la IP IPMI y la IP privada. No las mezcle.
2. No puede utilizar SSH o RDC para conectarse a la tarjeta IPMI; debe utilizar el software.
3. La IP IPMI y la IP privada se encuentran en la sección de hardware en cada **servidor**.
4. La tarjeta IPMI "escucha" la interfaz de IP privada y redirecciona el tráfico de IPMI a la tarjeta IPMI.

## Instrucciones de IPMI específicas de producto
{:#product-specific-impi-instructions}

* Para obtener más información sobre el uso de IPMI en una compartición CIFS, consulte [Montaje de una ISO en un servidor nativo](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-).
* Para obtener más información sobre el uso de IPMI con VMWare, consulte [Instalación de VMware vSphere ESXi mediante la consola remota y soportes virtuales](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi).

* Para obtener más información sobre el uso de IPMI con hardware IBM POWER, consulte [Instalación de IPMItool](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm).

**Aviso:**

Si inhabilita `eth0` (que es la interfaz de red privada), perderá todas las funcionalidades de IPMI, incluida la supervisión, la consola remota, el rearranque remoto, etc. Si desea bloquear el acceso a la interfaz privada, consulte la lista de direcciones IP permitidas que puede especificar en las tablas de IP o el cortafuegos del servidor.

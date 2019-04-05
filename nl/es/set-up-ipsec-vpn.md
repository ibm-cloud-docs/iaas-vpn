---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: IPSec VPN, IP address, IP traffic

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configurar la VPN IPSec
{:#setup-ipsec-vpn}

## ¿Qué es la VPN IPSec?
{:#what-is-ipsec-vpn}

IPSec es una suite de protocolos diseñada para autenticar y cifrar todo el tráfico de IP entre dos ubicaciones utilizando un modo de túnel que proporciona una red de sitio a sitio cifrada. Permite que los datos fiables pasen a través de redes que de lo contrario se considerarían no seguras.   Para obtener más información general acerca de la IPSec, consulte los [documentos de referencia](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation).


El acceso VPN de IBM Cloud permite a los usuarios gestionar todos los servidores de forma remota y segura en la red privada de IBM Cloud.  Una conexión VPN desde su ubicación a la red privada permite la gestión fuera de banda y el rescate de servidor a través de un túnel VPN cifrado.  Con el acceso VPN, puede:

   * Establecer una conexión VPN en la red privada mediante SSL o IPSEC.
   * Acceder al servidor con la dirección IP 10.x.x.x privada mediante SSH o RDP.
   * Conectarse a la dirección IP de IPMI del servidor para otras tareas de rescate y gestión de servidores.

Proporcionamos el servicio IPSec a los clientes para la gestión de los entornos. No se recomienda en las cargas de trabajo de producción.


## Configuración de una conexión IPSec
{:#setup-ipsec-connection}

### Parámetros de negociación
{:#setup-ipsec-vpn-negotiation-parameters}
![Parámetros de negociación](images/IPSec_VPN.png)

Necesitará conocer la siguiente información de la parte remota de la VPN IPSec:
- Dirección IP estática para el punto final de VPN
- Clave precompartida (contraseña)
- Algoritmo de cifrado(DES, 3DES, AES128, AES192, AES256)
- Autenticación (MD5, SHA1, SHA256, para las fases 1 y 2)
- Grupo Diffie-Hellman (para las fases 1 y 2)
- ¿Se utiliza el secreto-perfecto-adelante (PFS)?
- Tiempo de clave para la vida (para las fases 1 y 2) - **NOTA:** Nuestro sistema mide este valor en segundos.

Cuando esta información esté disponible, podrá configurar los parámetros de negociación básicos de la conexión VPN.

### Redes protegidas
{:#setup-ipsec-vpn-protected-networks}

En las propiedades de conexión de la VPN, debe definir las redes en el final remoto del túnel así como las redes locales del túnel. En "Subred de cliente (remoto) protegida", indique el espacio de dirección IP en la notación CIDR para el final remoto (no de IBM) del túnel IPSec.

<span style="text-decoration: underline">Por ejemplo:</span>  Si su red en el final remoto del túnel utiliza una única subred 10.0.0.0 con una máscara de red de 255.255.255.0, debería introducir una dirección IP 10.0.0.0 / CIDR 24 en la sección "Subred de cliente (remoto) protegida".

### Conversión de direcciones de red (NAT)
{:#setup-ipsec-vpn-nat}

Con la VPN IPSec, también puede definir direcciones IP privadas en la red de {{site.data.keyword.BluSoftlayer_notm}} que enviarán el tráfico a subredes remotas en el otro final de la conexión VPN.  Esto le permite reenviar el tráfico de Internet privado a una de sus direcciones IP internas de una máquina que se encuentre tras la VPN sin exponer la ubicación remota en el acceso a Internet completo.  

### Conversión de direcciones de red/Subredes de NAT estática asignadas
{:#setup-ipsec-vpn-nat-static-subnets}

Para configurar una IP de VPN remota con una entrada NAT estática: 

 * Seleccione la flecha roja para mostrar la lista de subredes en la sección **Subredes de NAT estática asignadas**. Se visualizará cada IP de la subred.  
 * Especifique la IP en el final remoto de la conexión VPN en la columna **IP de cliente** y escriba el nombre de la correlación en la columna **Nombre**.  
 * Seleccione **Añadir/modificar conversión de direcciones de contexto** y **Aplicar configuraciones** para guardar y aplicar la configuración.
 
Esta sección configura una conversión de red individual estática para el tráfico de retorno que utilizan los hosts del concentrador de VPN de IBM Cloud para comunicarse con los hosts de la VPN homóloga. Por ejemplo, todo el tráfico de la IP 10.1.255.92 se convertirá y reenviará a la IP 192.168.10.15 del cliente. Este reenvío elimina la necesidad de entradas de ruta adicionales en el servidor de IBM Cloud.

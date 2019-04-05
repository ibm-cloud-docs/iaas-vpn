---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# VPN con PPTP en desuso
{:#pptp-vpn-deprecation}

La VPN con PPTP está en desuso desde el 12 de junio de 2018, y ya no se ofrece a los clientes. Gracias por su interés. Para obtener más información sobre posibles alternativas, siga leyendo.

## ¿Qué es una VPN?
{:#pptp-vpn-deprecation-what-is-vpn}
El acceso VPN permite a los usuarios gestionar todos los servidores de forma remota y segura en la red privada de IBM Cloud. Una conexión VPN desde su ubicación a la red privada permite la gestión fuera de banda y el rescate de servidor a través de un túnel VPN cifrado. Con el acceso VPN, puede:

* Establecer una conexión VPN a la red privada mediante SSL, **PPTP** o IPSec.
* Acceder al servidor utilizando la dirección IP 10.x.x.x privada mediante SSH o RDP.
* Conectarse a la dirección IP de IPMI del servidor para otras tareas de rescate y gestión de servidores.

## PPTP en desuso
{:#pptp-deprecation-vpn}
Al volverse más seguras y versátiles otras opciones de VPN, la necesidad de PPTP ha disminuido. {{site.data.keyword.BluSoftlayer_notm}} proporciona otras opciones, como SSL o IPSec, que son más sofisticadas y protectoras que PPTP.

**Debido a estas razones, {{site.data.keyword.BluSoftlayer_notm}} ya no ofrece PPTP a partir del 12 de junio de 2018.**
{:important}


## Preguntas más frecuentes
{:#pptp-vpn-deprecation-faq}

**P: ¿Por qué PPTP está en desuso?**

**R:** Para proporcionar protección de la más alta calidad, {{site.data.keyword.BluSoftlayer_notm}} ha interrumpido el uso de PPTP. {{site.data.keyword.BluSoftlayer_notm}} desea mantener la promesa a nuestros clientes de que la seguridad de su privacidad y datos es de máxima importancia. 

**P: ¿Qué tipos de acceso VPN están disponibles aparte de PPTP?**

**R:** {{site.data.keyword.BluSoftlayer_notm}} ofrece varias opciones que solo requieren una configuración simple.
  1. La VPN con SSL es una conexión de acceso rápido que le conecta a nuestra red privada directamente desde un navegador. La VPN con SSL es compatible con Windows XP o posterior y con ActiveX, Fedora, Ubuntu y Mac OSX. El acceso global a nuestra red privada está disponible en un único URL que le permite elegir el punto final más cercano. Consulte [Configurar una conexión VPN con SSL](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) para obtener más detalles sobre cómo empezar con esta opción.
  2. IPSec es una suite de protocolos diseñados para autenticar y cifrara todo el tráfico de IP entre dos ubicaciones. Permite que los datos fiables pasen a través de redes que de lo contrario se considerarían no seguras. Para obtener más información general acerca de la IPSec, consulte [Configurar la VPN con IPSec](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) y otros [documentos de referencia](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation) para empezar a utilizar este servicio. 

**P: ¿Qué pasa si mis prácticas empresariales requieren PPTP?**

**R:** Hay disponibles varias opciones si se requiere PPTP para sus necesidades empresariales. **Aquí no se engloban todas las posibles opciones. Tenga en cuenta que las siguientes opciones requieren una configuración completa en ambos puntos finales. El cliente es responsable de la configuración de estas opciones.**
  1. Virtual Router Appliance. Virtual Router Appliance, también conocido como Vyatta, sirve como pasarela y direccionador de su entorno. Contienen zonas que constan de subredes. Se establece reglas de cortafuegos entre las zonas para comunicarse entre sí. Para las zonas que no necesitan comunicarse con otras zonas, no es necesaria ninguna regla de cortafuegos, ya que se descartan todos los paquetes. Consulte [Iniciación a Virtual Router Appliance](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance) para obtener más detalles sobre cómo iniciar este servicio. 
  2. Cortafuegos FSA. FortiGate Security Appliance (FSA) de 10 Gbps es un cortafuegos de hardware que puede configurarse para proteger el tráfico en varias VLAN, tanto para redes públicas como privadas. En el Portal de clientes se denomina “Cortafuegos de varias VLAN”. Consulte [Iniciación a FSA de 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) para obtener más detalles sobre la iniciación de este servicio. 
 
Las opciones anteriores son algunas posibilidades que puede explorar si necesita PPTP para sus necesidades empresariales, después de que el servicio ya no sea proporcionado por {{site.data.keyword.BluSoftlayer_notm}}. Agradecemos su confianza.
{:note}

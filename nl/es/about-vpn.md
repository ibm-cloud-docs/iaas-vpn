---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca de la VPN
{:#about-iaas-vpn}

El acceso VPN permite gestionar de forma remota todos los servidores y servicios relacionados con su cuenta en la red privada de IBM Cloud. Una conexión VPN desde su ubicación a la red privada permite **la gestión fuera de banda y el rescate de servidor** a través de un túnel VPN cifrado.

La comunicación mediante la red privada es más segura. Le proporciona flexibilidad para limitar el acceso público y, al mismo tiempo, le permite gestionar los servidores. Cualquier usuario de la cuenta puede recibir acceso VPN, que está disponible con SSL. Las interacciones de la VPN mediante el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) permiten la personalización del acceso VPN a nivel de usuario.

## Maneras de utilizar la VPN con SSL
{:#ways-to-use-iaas-vpn}

Esta pasarela segura fuera de banda le proporciona acceso al servidor a través de la red privada. Los usos más comunes son:

* Conectar direcciones IP privadas del servidor (10.x.x.x) en SSH o RDC.
* Conectar la tarjeta IPMI para la supervisión/consola/acceso remotos.
* Montar unidades en Windows o Red Hat desde el equipo doméstico o del trabajo para su comodidad.
* Cerrar interfaces públicas en servidores de base de datos y gestionar la red privada.
* Cerrar interfaces públicas y, al mismo tiempo, configurar el servidor por primera vez.
* Cerrar interfaces públicas durante las actualizaciones de seguridad críticas.
* Cerrar interfaces públicas durante la brecha de seguridad y resolver problemas en la red privada.

## Características principales
{:#iaas-vpn-key-features}

 * Nuestra red privada le proporciona una forma gratuita de comunicarse con los servidores y de gestionarlos. La VPN es la pasarela a esta red privada.
 * Los puntos de acceso de todo el mundo crean el mejor y más rápido acceso e interacción posibles. Actualmente, IBM Cloud dispone de puntos de acceso VPN en muchas ciudades.
 * Visite http://www.softlayer.com/vpn-access para obtener una lista de los puntos de acceso a la VPN de {{site.data.keyword.BluSoftlayer_notm}}.

## Cómo funciona
{:#iaas-vpn-how-it-works}

Con el acceso a VPN, se utiliza SSL para conectarse a la red privada y gestionar el servidor y los servicios. 

## Conexiones VPN con SSL
{:#iaas-vpn-ssl-vpn-connections}

La VPN con SSL es una conexión de acceso rápido que le conecta a nuestra red privada directamente desde un navegador. La VPN con SSL es compatible con Windows XP o posterior y con ActiveX, Fedora, Ubuntu y Mac OSX. El acceso global a nuestra red privada está disponible en un único URL que le permite elegir el punto final más cercano.

## Límite de subred VPN con SSL
{:#iaas-vpn-ssl-vpn-subnet-limit}

El cliente VPN con SSL tiene un límite estricto de subred 64 que se puede utilizar para completar la tabla de direccionamiento. Si su cuenta tiene más de 64 subredes, asegúrese de modificar los permisos VPN con SSL para utilizar la asignación de subred. Si no lo hace, algunas subredes pueden llegar a ser inalcanzables mediante la VPN con SSL.

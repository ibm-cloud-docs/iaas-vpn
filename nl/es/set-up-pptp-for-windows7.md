---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar la VPN con PPTP en Windows 7

La conexión VPN con PPTP permite una conexión remota a la red privada de {{site.data.keyword.BluSoftlayer_notm}} desde un escritorio o un dispositivo dedicado. La conexión a la red privada mediante PPTP está disponible para varios sistemas operativos, incluido Windows 7. Los usuarios pueden conectarse a cualquier centro de datos de {{site.data.keyword.BluSoftlayer_notm}} especificando la dirección de destino única del centro de datos durante la configuración. Siga los pasos siguientes para configurar una conexión VPN con PPTP en Windows 7.

## Configurar una conexión VPN con PPTP

1. Consulte la [página de procedimiento](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} para llegar a la pantalla de configuración de la conexión remota.

2. Especifique la dirección de destino del centro de datos deseado en el campo Dirección de Internet. Consulte la tabla siguiente para las direcciones adecuadas de los centros de datos de IBM Cloud actuales.

|Ubicación del centro de datos|Dirección de Internet del centro de datos|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San José, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapur, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, HK|pptpvpn.hkg02.softlayer.com|
|Melbourne, AU|pptpvpn.mel01.softlayer.com|
|Londres, GB|pptpvpn.lon02.softlayer.com|
|París, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tokio, JP|pptpvpn.tok02.softlayer.com|

3\. Especifique un nombre identificativo para la conexión en el campo **Nombre de destino**.

**Nota:** recomendamos utilizar la ubicación del centro de datos como nombre de destino.

4\. Especifique su nombre de usuario del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) en el campo **Nombre de usuario**.

5\. Especifique la **contraseña de VPN** en el campo **Contraseña**.

6\. Pulse el botón **Conectar**.

7\. En el sistema, tendrá que inhabilitar la pasarela remota para poder conectarse a Internet y a la VPN.

8\. Pulse **Iniciar**, abra **Panel de control** -> **Red y compartición** -> **Cambiar valores de adaptador**.

9\. Pulse con el botón derecho del ratón en la conexión VPN con PPTP y seleccione **Propiedades**.

10\. Desmarque el recuadro TCP/IPv6 y, a continuación, pulse TCP/IPv4 y después Propiedades.

11\. Pulse el botón **Avanzado**.

12\. Desmarque el recuadro **Utilizar pasarela predeterminada en la red remota** y, a continuación, seleccione **Aceptar**.

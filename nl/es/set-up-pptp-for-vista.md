---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar una VPN con PPTP en Windows Vista

La conexión VPN con PPTP permite una conexión remota a la red privada de {{site.data.keyword.BluSoftlayer_notm}} desde un escritorio o un dispositivo dedicado. La conexión a la red privada mediante el PPTP está disponible para varios sistemas operativos, incluido Windows Vista. Los usuarios pueden conectarse a cualquier centro de datos de {{site.data.keyword.BluSoftlayer_notm}} especificando la dirección de destino única del centro de datos durante la configuración. Siga los pasos siguientes para configurar una conexión VPN con PPTP en Windows Vista.

## Configurar una conexión VPN con PPTP

1. Consulte la [página de procedimiento](http://windows.microsoft.com/en-US/windows-vista/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} para llegar a la pantalla de configuración de la conexión remota.

2. Especifique la dirección de destino del centro de datos deseado en el campo Dirección de Internet.  Consulte la tabla siguiente para obtener las direcciones correctas de los centros de datos de {{site.data.keyword.BluSoftlayer_notm}} actuales.

|Ubicación del centro de datos|Dirección de Internet del centro de datos|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San José, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdam, NL|pptpvpn.ams01.softlayer.com|
|Singapur, SG|pptpvpn.sng01.softlayer.com|

3. Especifique un nombre identificativo para la conexión en el campo **Nombre de destino**.

**Nota:** recomendamos utilizar la ubicación del centro de datos como nombre de destino.

4. Especifique el **nombre de usuario del Portal del cliente** en el campo Nombre de usuario.

5. Especifique la **contraseña del Portal del cliente** en el campo Contraseña.

6. Pulse el botón **Conectar**.

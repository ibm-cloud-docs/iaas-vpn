---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar la VPN con PPTP para Mac OS X 10.X

La conexión VPN con PPTP permite una conexión remota a la red privada de {{site.data.keyword.BluSoftlayer_notm}} desde un escritorio o un dispositivo dedicado. La conexión a una red privada mediante PPTP está disponible para varios sistemas operativos, incluido Mac OS X. Los usuarios pueden conectarse a cualquier centro de datos de {{site.data.keyword.BluSoftlayer_notm}} especificando la dirección de destino única del centro de datos durante la configuración.  Siga los pasos siguientes para configurar una conexión VPN con PPTP en Mac OS X.

## Configurar una conexión VPN con PPTP

* Seleccione **Preferencias del sistema** en el desplegable **Menú de Apple**.
* Pulse el icono **Red** en la sección Internet y red.
* Pulse el icono del **signo más** en la parte inferior del menú **Conexiones**.  Aparecerá un recuadro emergente que le permitirá crear la conexión VPN.
* Cree la conexión VPN.
  * Seleccione **VPN** de la lista desplegable **Interfaz**.
  * Seleccione **PPTP** de la lista desplegable **Tipo de VPN**.
  * Especifique un **título descriptivo** para la conexión en el campo **Nombre de servicio**.
  * **Nota:** recomendamos utilizar la ubicación del centro de datos como parte del nombre de servicio.
  * Pulse el botón **Crear**.
* Haga clic en la conexión que acaba de crear en el menú Conexiones.
* Especifique la **dirección de destino** del centro de datos deseado en el campo **Dirección de servidor**.  Consulte la tabla siguiente para obtener las direcciones correctas de los centros de datos de {{site.data.keyword.BluSoftlayer_notm}} actuales.
* Especifique el **nombre de usuario del portal del cliente** en el campo **Nombre de cuenta**.
* Complete los Ajustes de autenticación.
  * Pulse el botón **Valores de autenticación**.  Aparecerá un recuadro emergente que le solicitará la autenticación de la VPN.
  * Especifique la **contraseña VPN de cliente** en el campo **Contraseña**.
  * Pulse el botón **Aceptar**.
* Actualice la configuración de tráfico VPN.
  * Pulse el botón **Avanzado**.
  * Asegúrese de que el recuadro de selección **Enviar todo el tráfico mediante la conexión VPN** de la sección Sesión está marcado.
  * Pulse el botón **Aceptar**.
* Seleccione el recuadro de selección **Mostrar el estado de la VPN en la barra de menús**.
* Pulse el botón Aplicar.  Es posible que la conexión VPN ya se haya establecido utilizando el elemento de barra de menús de la VPN.

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

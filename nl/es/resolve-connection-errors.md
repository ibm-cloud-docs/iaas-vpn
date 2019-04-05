---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN, Internet Explorer caching, Internet Explorer, Windows

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Resolver errores de conexión a la VPN con SSL en Windows
{:#resolve-errors-connecting-to-ssl-vpn-with-windows}

Si obtiene errores al conectarse a la VPN con SSL en Windows, puede resolverlos con los pasos siguientes:

1. Compruebe si tiene las credenciales y los permisos SSL apropiados en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
2. Compruebe la hora/fecha/huso horario/horario de verano de su sistema.
3. Debe aceptar e instalar el applet de ActiveX.
4. Desactive los bloqueadores de ventanas emergentes ya que pueden bloquear el applet de ActiveX.
5. Compruebe los cortafuegos personales ya que permiten el uso de ActiveX.
6. Permita el almacenamiento en memoria caché de Internet Explorer. En Internet Explorer, seleccione **Herramientas->Internet**, a continuación, **Opciones->Valores**.
7. Utilice solo el navegador Internet Explorer (IE) (compruebe si hay actualizaciones).
8. Intente rearrancar el sistema.

Cuando se haya conectado correctamente, aparecerá una "A" en la bandeja del sistema.

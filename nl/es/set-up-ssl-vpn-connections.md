---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar conexiones VPN con SSL

Windows, Linux Fedora, y Linux requieren instrucciones de conexión individuales que se muestran en este documento. Estos son algunos de los ejemplos sobre cómo utilizar una conexión VPN con SSL:

* Escritorio remoto a la dirección IP de fondo de su servidor (10.4.X.X) para la administración de sus servidores Windows 2003.
* SSH a la dirección IP de fondo de vuestro servidor (10.4.X.X) para administrar los servidores UNIX.
* Utilice un cliente IPMI para controlar el servidor utilizando la dirección IPMI de fondo (10.4.X.X). Puede descargar la herramienta de cliente IPMI cuando se haya conectado a http://downloads.service.softlayer.com.
  * **Nota:** IPMIView requiere que Java esté instalado.  http://www.sun.com/java/
* Prueba del sitio web en las IP de fondo antes de que aparezca en sus IP públicas.
* Transferencia de archivos de datos seguros entre sus servidores y su casa/oficina.
* Copia de seguridad de los archivos de configuración de su servidor en casa o en la oficina.
* Conexión segura a nuestro portal web http://manage.service.softlayer.com.

## Windows (Internet Explorer)

1. Abra Internet Explorer y vaya a http://www.softlayer.com/vpn-access.
* Cuando haya especificado su nombre de usuario y contraseña, se le solicitará instalar un plugin de ActiveX. Debe instalar el plugin para conectarse a la red de fondo. 
* También debe tener derechos administrativos en la estación de trabajo para instalar el plugin de ActiveX. Si no está autorizado a instalar el conector, solicite al administrador de sistemas local que lo instale. 
* Cuando haya instalado el plugin de ActiveX, una matriz de VPN con SSL se iniciará y establecerá una conexión con el dispositivo VPN. Si lo hace correctamente, aparecerá una '**A**' de color rojo en la barra de tareas. Puede pulsar en la '**A**' en cualquier momento para ver el estado de la conexión VPN con SSL: el estado, la dirección IP asignada, los servidores DNS asignados, las rutas de red y el tiempo que ha estado conectado. 
* Puede minimizar la sesión de navegador en cualquier momento y seguir utilizando otras aplicaciones de forma segura en la red privada. 
* Cuando haya terminado, desconéctese seleccionando el botón de desconexión de la derecha o cierre la ventana.

## Linux Fedora (FireFox)

Se recomienda ejecutar todos los mandatos como root. (`setuid root`)

1. Descargue Java desde `http://java.com/en/download/manual.jsp`. Se trata de un archivo autoextraíble de Linux.
* Cierre FireFox.
* Mueva el archivo al sitio en el que desea instalar Java (normalmente `/usr/local`)
* Convierta el archivo en ejecutable utilizando el mandato `chmod +x jre-6u1-linux-i586.bin`
* Ejecute el instalador utilizando el mandato `./jre-6u1-linux-i586.bin`
* Acepte los términos y realice la instalación.
* Cuando finalice la instalación, cree un enlace simbólico.

## Ejemplo de Linux
```
cd /usr/lib/firefox-1.0.4/plugins/
ln -s /usr/local/jre-6u1/plugin/i386/ns7/libjavaplugin_oji.so .
```

1. Abra Firefox y vaya a `http://www.softlayer.com/vpn-access`.
* Inicie sesión con su nombre de usuario y contraseña del portal del cliente.
* Cuando se haya conectado, seleccione el separador **Red**.
* Debería ver el botón conectar/instalar. Selecciónelo y se le solicitará instalar un componente Java.
* Deje que el componente se instale en la vía de acceso predeterminada, que es posible que tenga que crear manualmente. (`/usr/local/array_vpn`)
* Cuando se haya instalado, aparecerá una ventana que le indicará que está conectado.
* La ventana debe permanecer abierta para utilizar el túnel VPN, pero puede minimizarla.
* Para probar la conexión, haga ping en 10.0.80.11 o en la dirección privada de su servidor. Si obtiene una respuesta, eso significa que se ha conectado correctamente.
* Cuando haya terminado, seleccione el botón de desconexión en el separador 'Red' o cierre todas las ventanas del navegador.

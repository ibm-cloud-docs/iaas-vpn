---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Clientes VPN autónomos - Windows, Linux y Mac OS X

## Cliente autónomo de Windows

Windows (8/7/Vista/XP) de 32 bits:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win32_v1.1.3.zip

Windows (8/7/Vista/XP) de 64 bits:  https://speedtest.dal05.softlayer.com/array/ArrayMotionProSetup_win64_v1.1.3.zip

1. Descargue uno de los archivos listados más arriba en función de su sistema operativo.
* Ejecute MotionProSetup para instalar el software.
* Ejecute MotionPro y en la pantalla inicial seleccione **Perfil -> Añadir**.
* Cree un perfil y proporciónele un nombre de sitio, seleccionando un nombre de host de la lista de sitios de VPN con SSL (más abajo). A continuación, especifique su nombre de usuario y contraseña de VPN y pulse **Guardar**.
* Por último, efectúe una doble pulsación en el perfil que ha creado para conectarse a la VPN.

**Notas**
 * 'Sitio' puede ser un nombre de dominio o una dirección IP.
 * Si tiene problemas, desinstale los programas matriz que utilizan el panel de control de Windows, rearranque y vuelva a conectarse.
 * No funciona en Windows 8 RT.

## Cliente autónomo de Linux

CentOS de 64 bits: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_CentOS_x86-64_1.0.4.sh

Redhat de 32 bits: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-32_1.0.4.sh

Redhat de 64 bits: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_RedHat_x86-64_1.0.4.sh

Ubuntu de 32 bits: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-32_1.0.4.sh

Ubuntu de 64 bits: https://speedtest.dal05.softlayer.com/array/MotionPro_Linux_Ubuntu_x86-64_1.0.4.sh

1. Conviértalo en ejecutable: `chmod +x MotionPro_Linux_CentOS_x86-64_1.0.4.sh`
* Ejecute el script: `./MotionPro_Linux_CentOS_x86-64_1.0.4.sh.`
* Uso: `./MotionPro --host [site] --user [username] --passwd [password]`
* Para detenerlo: `[control-c]`

**Notas:**  
 * Para iniciar el cliente MotionPro, debe entrar al menos `hostname` y `username` como argumentos.
 * 'Sitio' puede ser un nombre de dominio o una dirección IP.

## Cliente autónomo de Mac OS X 10.10

Pasos para la VPN con SSL matriz autónoma del cliente Motion Pro Plus para MacOS:

1. Instale el cliente "Motion Pro Plus" desde la Apple store.
* Localice el cliente Motion Pro Plus en la carpeta Aplicaciones y abra la aplicación.
* Pulse Perfil y Añadir.
* Rellene el nombre del sitio, el host y el nombre de usuario y pulse Aceptar.
* Seleccione la VPN en la parte superior izquierda y conéctese.

A continuación, se ofrece un ejemplo:

![Figura 1](images/snip20170425_1.png)

Si el túnel no dirige el tráfico correctamente, es posible que deba [añadir rutas manualmente](https://discussions.apple.com/thread/2735376).

*Desinstale las versiones anteriores antes de actualizar.*

## POP de VPN con SSL (sitios)

* vpn.ams01.softlayer.com
* vpn.ams03.softlayer.com
* vpn.dal01.softlayer.com
* vpn.dal05.softlayer.com
* vpn.dal06.softlayer.com
* vpn.dal07.softlayer.com
* vpn.dal09.softlayer.com
* vpn.sea01.softlayer.com
* vpn.wdc01.softlayer.com
* vpn.wdc04.softlayer.com
* vpn.hou02.softlayer.com
* vpn.sjc01.softlayer.com
* vpn.sjc03.softlayer.com
* vpn.sng01.softlayer.com
* vpn.atl01.softlayer.com
* vpn.chi01.softlayer.com
* vpn.den01.softlayer.com
* vpn.lax01.softlayer.com
* vpn.mia01.softlayer.com
* vpn.nyc01.softlayer.com
* vpn.hkg02.softlayer.com
* vpn.lon02.softlayer.com
* vpn.sao01.softlayer.com
* vpn.mil01.softlayer.com
* vpn.mel01.softlayer.com
* vpn.tor01.softlayer.com
* vpn.mex01.softlayer.com
* vpn.fra02.softlayer.com
* vpn.par01.softlayer.com
* vpn.syd01.softlayer.com
* vpn.che01.softlayer.com
* vpn.mon01.softlayer.com
* vpn.tok02.softlayer.com


**Tenga en cuenta lo siguiente: Desinstale las versiones anteriores del cliente antes de instalar la versión nueva.**

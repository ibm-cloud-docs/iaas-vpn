---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar PPTP para Fedora Core 5

Deberá realizar la instalación y configuración.

**1. Instalación**
Instale el PPTP y la interfaz gráfica de usuario `pptpconfig` utilizando uno de los mandatos siguientes:
```
# rpm -Uvh http://pptpclient.sourceforge.net/yum/stable/fc5/pptp-release-current.no...
# yum --enablerepo=pptp-stable install pptpconfig
```

**2. Configuración**

1. Información sobre el PPTP de IBM Cloud:
<table><tr><td>Servidor:</td><td>pptpvpn.dal01.softlayer.com (Dallas)<br/>pptpvpn.sea01.softlayer.com (Seattle)<br/>pptpvpn.wdc01.softlayer.com (Washington D.C.)</td></tr><tr><td>Nombre de dominio:</td><td>Dejar en blanco</td></tr><tr><td>Nombre usuario:</td><td>(ejemplo: SL12345)</td></tr><tr><td>Contraseña:</td><td>&nbsp;</td></tr></table>

2. Ejecute *pptpconfig* <span style="text-decoration: underline">como root</span>; debería aparecer una ventana,<br/>
![Figura 1](images/ss1.jpeg)

3. Escriba el nombre, servidor, nombre de usuario y contraseña en el separador Servidor.

4. En la sección Cifrado, deje todo tal y como aparece de forma predeterminada, puesto que funciona para la mayoría de los clientes.<br/>
![Figura 2](images/ss2.jpeg)

5. Pulse en *Añadir*; el túnel aparecerá en la lista,

6. Pulse en el túnel para seleccionarlo y, a continuación, en *Iniciar*; aparecerá una ventana con el registro y estado de la conexión de túnel.

7. Si la conexión falla, tendrá que recopilar más información, por lo que en el separador *Varios*, pulse *Habilitar los recursos de depuración de conexión*, pulse *Actualizar*, intente *Iniciar* de nuevo y, a continuación, vaya a [Diagnóstico CÓMO](http://pptpclient.sourceforge.net/howto-diagnosis.phtml){:new_window} para cualquier error que se muestre.<br/>
![Figura 3](images/ss3.jpeg)

8. Si la conexión se ha realizado correctamente, puede probar el botón Prueba del ping. Si el ping falla, debería intentar averiguar la razón antes de continuar. Si el ping funciona, el túnel se activa y podrá trabajar en el direccionamiento.

9. Solo se deberían direccionar a través del túnel de VPN las IP que se encuentran en la red de fondo de IBM Cloud.  *Detenga* el túnel, selecciónelo de nuevo y, a continuación, pulse *Cliente a LAN o LAN a LAN* en el separador *Direccionamiento*; utilice el botón *Editar rutas de red*, introduzca '10.0.0.0/8' en Red y 'SoftLayer' en Nombre, e intente *Iniciar* de nuevo. Ahora intente acceder a la dirección IP privada del servidor o al servidor de nombres privado de SoftLayer en 10.0.80.11.<br/>
![Figura 4](images/ss4.jpeg)

---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuração da VPN PPTP para Windows Vista

A conexão de VPN do PPTP permite a conexão remota com a {{site.data.keyword.BluSoftlayer_notm}} Rede privada por meio de uma área de trabalho ou um dispositivo dedicado. 
A conexão com a rede privada por meio de PPTP está disponível para múltiplos sistemas operacionais, incluindo o Windows Vista. Os usuários podem se conectar de qualquer data center do {{site.data.keyword.BluSoftlayer_notm}} inserindo o endereço de destino exclusivo do data center durante a configuração. 
Siga as etapas abaixo para configurar uma conexão VPN PPTP no Windows Vista.

## Configure uma conexão de VPN do PPTP

1. Consulte a
[Página
de Instruções](http://windows.microsoft.com/en-US/windows-vista/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} da Microsoft para acessar a tela para configurar a conexão remota.

2. Insira o endereço de destino do data center desejado no campo de endereço de Internet. Consulte a tabela abaixo para obter os endereços apropriados para data centers atuais do {{site.data.keyword.BluSoftlayer_notm}}.

|Local do Data Center|Endereço de Internet do Data Center|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdã, Holanda|pptpvpn.ams01.softlayer.com|
|Cingapura, SG|pptpvpn.sng01.softlayer.com|

3. Insira um nome de identificação para a conexão no campo **Nome do destino**.

**Nota:** recomendamos usar o local do data center como o nome do destino.

4. Insira seu **Nome do usuário do Portal do cliente** no campo Nome do usuário.

5. Insira sua **Senha do Portal do cliente** no campo Senha.

6. Clique no botão **Conectar**.

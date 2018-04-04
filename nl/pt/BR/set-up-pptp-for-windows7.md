---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuração da VPN PPTP para Windows 7

A conexão de VPN do PPTP permite a conexão remota com a {{site.data.keyword.BluSoftlayer_notm}} Rede privada por meio de uma área de trabalho ou um dispositivo dedicado. A conexão à rede privada por meio de PPTP está disponível para múltiplos sistemas operacionais, incluindo Windows 7. Os usuários podem se conectar a qualquer data center {{site.data.keyword.BluSoftlayer_notm}} inserindo o endereço de destino exclusivo do data center durante a configuração. Siga as etapas abaixo para configurar uma conexão VPN PPTP no Windows 7.

## Configure uma conexão VPN do PPTP

1. Consulte a [Página de instruções](http://windows.microsoft.com/en-US/windows7/Set-up-a-remote-connection-to-your-workplace-using-VPN){:new_window} da Microsoft para acessar a tela para configurar a conexão remota.

2. Insira o endereço de destino do data center desejado no campo de endereço de Internet. Consulte a tabela abaixo para os endereços apropriados para os data centers do IBM Cloud atuais.

|Local do Data Center|Endereço de Internet do Data Center|
|---|---|
|Dallas, TX|pptpvpn.dal01.softlayer.com|
|Seattle, WA|pptpvpn.sea01.softlayer.com|
|San Jose, CA|pptpvpn.sjc01.softlayer.com|
|Washington, DC|pptpvpn.wdc01.softlayer.com|
|Amsterdã, Holanda|pptpvpn.ams01.softlayer.com|
|Cingapura, SG|pptpvpn.sng01.softlayer.com|
|Houston, TX|pptpvpn.hou02.softlayer.com|
|Hong Kong, Hong Kong|pptpvpn.hkg02.softlayer.com|
|Melbourne, Austrália|pptpvpn.mel01.softlayer.com|
|Londres, GB|pptpvpn.lon02.softlayer.com|
|Paris, FR|pptpvpn.par01.softlayer.com|
|Toronto, CA|pptpvpn.tor01.softlayer.com|
|Tóquio, JP|pptpvpn.tok02.softlayer.com|

3\. Insira um nome de identificação para a conexão no campo **Nome do destino**.

**Nota:** recomendamos usar o local do data center como o nome do Destino.

4\. Insira seu [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) nome do usuário no campo **Nome do usuário**.

5\. Insira sua **Senha do VPN** no campo **Senha**.

6\. Clique no botão **Conectar**.

7\. Agora, em seu computador, desative o gateway remoto para poder se conectar à Internet e à VPN.

8\. Clique em **Iniciar**, em seguida, abra o **Painel de controle** -> **Rede e compartilhamento** -> **Mudar configurações do adaptador**.

9\. Clique com o botão direito na conexão VPN PPTP e clique em **Propriedades**.

10\. Desmarque a caixa TCP/IPv6 e, depois, clique em TCP/IPv4 e clique em Propriedades.

11\. Clique no botão **Avançado**.

12\. Desmarque a caixa para **Usar gateway padrão na rede remota** e, em seguida, selecione **OK**.

---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-09"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuração da VPN PPTP para Mac OS X 10.X

A conexão de VPN do PPTP permite a conexão remota com a {{site.data.keyword.BluSoftlayer_notm}} Rede privada por meio de uma área de trabalho ou um dispositivo dedicado. 
A conexão com a rede privada por meio do PPTP está disponível para múltiplos sistemas operacionais, incluindo o Mac OS X. Os usuários
podem se conectar a qualquer data center {{site.data.keyword.BluSoftlayer_notm}} inserindo o endereço de destino exclusivo
do data center na configuração. Siga as etapas abaixo para configurar uma conexão VPN PPTP no Mac OS X.

## Configure uma conexão de VPN do PPTP

* Selecione **Preferências do sistema** no **Menu da Apple** suspenso.
* Clique no ícone **Rede** na seção Internet e Rede.
* Clique no ícone **Sinal de mais** na parte inferior no menu **Conexões**. Uma caixa pop-up aparece para permitir que você crie a conexão VPN.
* Crie a conexão VPN.
  * Selecione **VPN** na lista suspensa **Interface**.
  * Selecione **PPTP** na lista suspensa **Tipos de VPN**.
  * Insira um **título descritivo** para a conexão no campo **Nome do serviço**.
  * **Nota:** recomendamos usar o local do data center como parte do Nome do serviço.
  * Clique no botão **Criar**.
* Clique na conexão recém-criada no menu Conexões.
* Insira o **endereço de destino** do data center desejado no campo **Endereço do servidor**. Consulte a tabela abaixo para obter os endereços apropriados para data centers atuais do {{site.data.keyword.BluSoftlayer_notm}}.
* Insira seu **Nome do usuário do Portal do cliente** no campo **Nome da conta**.
* Conclua as configurações de autenticação.
  * Clique no botão **Configurações de autenticação**. Uma caixa pop-up aparecerá solicitando autenticação da VPN.
  * Insira sua **Senha da VPN do cliente** no campo **Senha**.
  * Clique no botão **OK**.
* Atualize as configurações de tráfego da VPN.
  * Clique no botão **Avançado**.
  * A caixa de seleção **Enviar todo o tráfego por meio da conexão VPN** na seção Sessão não deve estar selecionada.
  * Clique no botão **OK**.
* Selecione a caixa de seleção **Mostrar status da VPN na barra de menus**.
* Clique no botão Aplicar. A conexão VPN agora pode ser estabelecida a qualquer momento usando o item da barra de menus VPN.

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

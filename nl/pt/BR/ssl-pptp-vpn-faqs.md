---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Perguntas frequentes sobre a VPN

## O que é a VPN do IBM Cloud?

O acesso de VPN do IBM Cloud é projetado para permitir que os usuários gerenciem remotamente todos os servidores com segurança na rede privada do IBM Cloud.  Uma conexão de VPN de sua localização para a rede privada permite o gerenciamento fora da banda e o resgate do servidor por meio de um túnel VPN criptografado. Com o acesso de VPN, é possível:

* Estabeleça uma conexão de VPN com a rede privada usando SSL, PPTP ou IPSEC
* Acesse o servidor por meio do endereço IP privado 10.x.x.x usando SSH ou RDP
* Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor adicional ou necessidades de resgate.


## A VPN de SSL também executa PPTP, IPSEC ou outros protocolos de VPN?

Atualmente, o gateway da VPN de SSL usa um plug-in da VPN de SSL baseado no navegador ou um cliente proprietário para criar conexões. Continuaremos a trazer mais opções de conectividade de VPN à rede privada. A VPN de SSL foi selecionada para facilitar o uso e a compatibilidade.


<a name="152"></a>
## Posso montar o servidor NAS/FTP da minha localização remota por meio do gateway da VPN SSL?

Não. Você só tem acesso à sua VLAN privada e aos servidores do gateway da VPN SSL. Se você quiser fazer download de dados do seu volume NAS/FTP, deverá movê-los para o servidor e depois transferi-los para o local remoto por meio da VPN.

Por motivos de segurança, apenas servidores localizados dentro do data center têm acesso permitido aos servidores que fornecem serviços (DNS, Atualização, NAS, Lockbox).

<a name="175"></a>
## Qual fornecedor produz a VPN SSL e como ela funciona?

Nosso gateway de VPN SSL é um produto de segurança do Array Networks.  O próprio gateway executa raio para atualizar usuários e senhas do nosso Portal do cliente. Se você deseja incluir usuários e dar a eles acesso à VPN SSL, crie um novo usuário dentro do Portal do cliente e ative as permissões da VPN SSL.

<a name="276"></a>
## Qual a diferença entre VPN SSL e PPTP?

A **VPN SSL** permite que um usuário crie um túnel seguro da área de trabalho remota para a
{{site.data.keyword.BluSoftlayer_notm}}Rede privada. Ela é compatível com uma variedade de sistemas operacionais.

A **VPN PPTP** permite o mesmo túnel seguro, mas se conecta usando o software de cliente especializado na área de trabalho ou dispositivo dedicado de um usuário. A VPN PPTP é uma boa solução para os usuários que não conseguem usar uma conexão SSL.

## Quando me conecto à VPN PPTP, ela informa "Erro 691: o acesso foi negado porque o nome de usuário e/ou senha é inválido." Como corrijo esse problema?

Todos os usuários têm a capacidade de se conectar à VPN PPTP, mas devem ter permissão para efetuar login por meio do Portal do cliente. As permissões da VPN PPTP são facilmente verificadas e atualizadas rapidamente. Consulte [Ativar ou desativar o acesso à VPN PPTP](activate-a-user.html) para obter informações adicionais.

## Por que não consigo incluir usuários adicionais para VPN do PPTP?

A VPN do PPTP está disponível em todas as contas, mas é inicialmente configurada para ativar o acesso para um usuário por vez. Para solicitar uma conta a ser ativada para PPTP ilimitado sem custo adicional, crie um chamado por meio do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) com as informações a seguir, juntamente com quaisquer detalhes adicionais que possam ser desejados:

* Tópico: Solicitação de VPN do PPTP
* Texto: eu atualmente tenho o PPTP limitado a um usuário por vez. Ative o acesso de VPN do PPTP ilimitado para a minha conta.

Um membro da equipe de suporte IBM atualizará a conta para ativar o acesso ao PPTP ilimitado, que está disponível sem custo adicional. O chamado será atualizado se qualquer informação adicional for necessária.

## Quais são as categorias disponíveis para o status de gerenciamento de um usuário da VPN no Portal do cliente?

As categorias de status do cliente incluem aquelas que podem ser atualizadas por um usuário e aquelas que podem aparecer automaticamente. Eles incluem:

* **Ativo** - o usuário tem acesso ao [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) e à VPN baseada em permissões configuradas pelo administrador de conta. Esse status pode ser selecionado manualmente ou mudado a qualquer momento.
* **Desativado** - o usuário não tem acesso a nenhuma permissão ou assinatura na conta, incluindo [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) e VPN. Se configurado como desativado por outro usuário na conta, esse status pode ser manualmente selecionado e/ou mudado a qualquer momento.
* **VPN Apenas** - o usuário só tem acesso à conectividade de VPN e não pode acessar o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Esse status pode ser selecionado manualmente ou mudado a qualquer momento.
* **Inativo** - o usuário não utilizou o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) ou a VPN nos últimos 60 dias. Esse é um status gerado pelo sistema.
* **cancel_pending** - um administrador na conta cancelou esse usuário e o cancelamento está sendo processado atualmente. Esse status é gerado pelo sistema.

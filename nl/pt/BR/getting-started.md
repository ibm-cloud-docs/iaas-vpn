---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introdução à rede privada virtual (VPN)

## O que é a VPN do IBM Cloud?

O acesso à VPN permite que os usuários gerenciem todos os servidores remotamente e com segurança na rede privada do IBM Cloud. Uma conexão VPN de sua localização para a rede privada permite transferências de arquivos ilimitadas, gerenciamento fora da banda e o resgate do servidor por meio de um túnel VPN criptografado. Com o acesso de VPN, é possível:

* Estabeleça uma conexão VPN com a rede privada por SSL, PPTP ou Internet Protocol Security
* Acesse o seu servidor por meio de seu endereço IP privado 10.x.x.x por SSH ou RDP
* Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor adicional ou necessidades de resgate.

Alguns serviços requerem acesso por meio de rede privada e a VPN é um método que permite acesso à rede privada. Uma VPN é boa para usar quando você precisa efetuar login na rede privada, fazer seu trabalho e, depois, efetuar logout. Por exemplo, esse acesso geralmente é necessário para atingir o KVM do servidor.

Cada conta do usuário pode receber acesso à VPN e pode ser limitada quanto às sub-redes que precisa de acesso. O acesso à VPN deve estar ativado e deve-se criar uma senha de VPN antes de efetuar login na VPN.

## Ativar o acesso à VPN de cada usuário

Para começar, você precisará ativar o acesso à VPN em cada conta que precisar desse acesso. Cada conta começa com o acesso à VPN **desativado**, incluindo a conta principal da sua equipe. Para ativar o acesso à VPN, siga estas etapas:

1. Acesse **Conta -> Acesso à VPN** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Ali você encontrará a linha para cada possível usuário de VPN e um link sob a coluna **Acesso à VPN**.
* O link indicará "Nenhum" se o usuário ainda não tiver o acesso à VPN ativado.
* Se o link de acesso à VPN do usuário for **SSL, PPTP ou SSL e PPTP**, o acesso do usuário à VPN já foi ativado.

![Tabela de acesso à VPN do Portal Softlayer](images/vpnaccess01.png)

1. Para ativar ou mudar os tipos de acesso à VPN permitidos para um usuário específico, clique no link sob a coluna
**Acesso à VPN**.
* Na próxima página, é possível ativar o tipo de acesso à VPN apropriado para cada usuário.  
* Por padrão, apenas um usuário pode ter acesso à VPN PPTP. Se sua conta requerer mais de um usuário de VPN PPTP, entre em contato com nossa equipe de suporte via bate-papo em tempo real, sistema de chamado ou por telefone para permitir usuários de VPN PPTP ilimitados sem custo.

![Designe o acesso do tipo VPN a um usuário](images/vpntype01.png)

## Configure a senha da VPN

Sua próxima etapa é criar uma senha da VPN. Cada usuário pode criar e atualizar sua senha da VPN no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Para fazer isso, selecione seu nome na parte superior direita, que o levará à página **Editar perfil**. Também é possível selecionar **Conta -> Usuários** e, em seguida, selecionar seu nome do usuário.

      Nota: o link indica "Usuário principal". Esse link indicará seu nome para sub-usuários.

Na página **Editar perfil do usuário**, basta rolar para baixo e inicializar ou atualizar a senha da VPN.

![ Editar campos de senha de VPN de perfil](images/vpnpasswordfields.png)

## Efetue login na VPN

Agora que o acesso à VPN foi estabelecido, é possível efetuar login.

1. Para efetuar login na VPN SSL, visite [vpn.softlayer.com](https://vpn.softlayer.com/) e selecione qualquer um dos pontos de login. É possível usar qualquer ponto de acesso à VPN e você terá as mesmas permissões de acesso à rede privada em todos os data centers.
* Se você tiver problemas de login em um local, tente outro local.
* Como alternativa, efetue login usando uma VPN SSL de cliente independente.
* Você poderá usar os utilitários padrão de S.O. para efetuar login na VPN PPTP.

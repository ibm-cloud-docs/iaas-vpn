---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, IBM Cloud VPN, user account

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Introdução à rede privada virtual (VPN)
{:#gettingstarted-with-virtual-private-networking}

## O que é a VPN do IBM Cloud?
{:#what-is-ibmcloud-vpn}


O acesso à VPN permite que os usuários gerenciem todos os servidores remotamente e com segurança na rede privada do IBM Cloud. Uma conexão de VPN de sua localização para a rede privada permite o gerenciamento fora da banda e o resgate do servidor por
meio de um túnel VPN criptografado. Com o acesso de VPN, é possível:

* Estabeleça uma conexão VPN com a rede privada por SSL ou IPSec.
* Acesse seu servidor por meio de seu endereço IP privado 10.x.x.x por SSH ou RDP.
* Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor adicional ou necessidades de resgate.

**Os serviços de VPN PPTP foram descontinuados em 12 de junho de 2018, conforme descrito em [nosso anúncio](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation).**
{:deprecated}

Alguns serviços requerem acesso por meio de rede privada e a VPN é um método que permite acesso à rede privada. Uma VPN é boa para usar quando você precisa efetuar login na rede privada, fazer seu trabalho e, depois, efetuar logout. Por exemplo, esse acesso geralmente é necessário para atingir o KVM do servidor.

Cada conta do usuário pode receber acesso à VPN e pode ser limitada quanto às sub-redes que precisa de acesso. O acesso à VPN deve estar ativado e deve-se criar uma senha de VPN antes de efetuar login na VPN.

## Ativar o acesso à VPN de cada usuário
{:#enable-user-vpn-access}

Para começar, você precisará ativar o acesso à VPN em cada conta que precisar desse acesso. Cada conta começa com o acesso à VPN **desativado**, incluindo a conta principal da sua equipe. Para ativar o acesso à VPN, siga estas etapas:

1. Acesse **Conta -> Acesso à VPN** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Ali você encontrará a linha para cada possível usuário de VPN e um link sob a coluna **Acesso à VPN**.
* O link indicará "Nenhum" se o usuário ainda não tiver o acesso à VPN ativado.
* Se o link de acesso à VPN do usuário é **SSL**, isso significa que o acesso do usuário à VPN já foi ativado.

![Tabela de acesso à VPN do Portal Softlayer](images/vpnaccess01.png)

1. Para ativar ou mudar os tipos de acesso à VPN permitidos para um usuário específico, clique no link sob a coluna
**Acesso à VPN**.
* Na próxima página, é possível ativar o tipo de acesso à VPN apropriado para cada usuário.  

![Designe o acesso do tipo VPN a um usuário](images/vpntype01.png)

## Configure a senha da VPN
{:#set-vpn-password}

Sua próxima etapa é criar uma senha da VPN. Cada usuário pode criar e atualizar sua senha da VPN no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Para fazer isso, selecione seu nome na parte superior direita, que o levará à página **Editar perfil**. Também é possível selecionar **Conta -> Usuários** e, em seguida, selecionar seu nome do usuário.

      Nota: o link indica "Usuário principal". Esse link indicará seu nome para sub-usuários.

Na página **Editar perfil do usuário**, basta rolar para baixo e inicializar ou atualizar a senha da VPN.

![ Editar campos de senha de VPN de perfil](images/vpnpasswordfields.png)

## Efetue login na VPN
{:#login-to-the-vpn}

Agora que o acesso à VPN foi estabelecido, é possível efetuar login.

1. Para efetuar login na VPN SSL, visite [vpn.softlayer.com](https://vpn.softlayer.com/) e selecione qualquer um dos pontos de login. É possível usar qualquer ponto de acesso à VPN e você terá as mesmas permissões de acesso à rede privada em todos os data centers.
* Se você tiver problemas de login em um local, tente outro local.
* Como alternativa, efetue login usando uma VPN SSL de cliente independente.

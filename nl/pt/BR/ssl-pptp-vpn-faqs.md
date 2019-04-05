---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN FAQ, IBM Cloud VPN access, IBM Cloud VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}

# Perguntas frequentes sobre a VPN
{:#vpn-faq}

## O que é a VPN do IBM Cloud?
{:#what-is-ibm-cloud-vpn}
{:faq}

O acesso de VPN do IBM Cloud é projetado para permitir que os usuários gerenciem remotamente todos os servidores com segurança na rede privada do IBM Cloud.  Uma conexão de VPN de sua localização para a rede privada permite o gerenciamento fora da banda e o resgate do servidor por meio de um túnel VPN criptografado. Com o acesso de VPN, é possível:

* Estabeleça uma conexão de VPN com a rede privada usando SSL ou IPSEC
* Acesse o servidor por meio do endereço IP privado 10.x.x.x usando SSH ou RDP
* Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor adicional ou necessidades de resgate.


## A VPN de SSL também executa PPTP, IPSEC ou outros protocolos de VPN?
{:#does-ssl-vpn-perform-pptp-ipsed-vpn-protocols}
{:faq}

Atualmente, o gateway da VPN de SSL usa um plug-in da VPN de SSL baseado no navegador ou um cliente proprietário para criar conexões. Continuaremos a trazer mais opções de conectividade de VPN à rede privada. A VPN de SSL foi selecionada para facilitar o uso e a compatibilidade. O PPTP foi descontinuado. Consulte [Descontinuação da VPN do PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obter mais informações.



## Posso montar o servidor NAS/FTP da minha localização remota por meio do gateway da VPN SSL?
{:#can-i-mount-nas-ftp-remotely}
{:faq}

Não. Você só tem acesso à sua VLAN privada e aos servidores do gateway da VPN SSL. Se você quiser fazer download de dados do seu volume NAS/FTP, deverá movê-los para o servidor e depois transferi-los para o local remoto por meio da VPN.

Por motivos de segurança, apenas servidores localizados dentro do data center têm acesso permitido aos servidores que fornecem serviços (DNS, Atualização, NAS, Lockbox).


## Qual fornecedor produz a VPN SSL e como ela funciona?
{:#what-vendor-makes-ssl-vpn}
{:faq}

Nosso gateway de VPN SSL é um produto de segurança do Array Networks.  O próprio gateway executa raio para atualizar usuários e senhas do nosso Portal do cliente. Se você deseja incluir usuários e dar a eles acesso à VPN SSL, crie um novo usuário dentro do Portal do cliente e ative as permissões da VPN SSL.


## Qual a diferença entre VPN SSL e PPTP?
{:#what-is-the-difference-between-ssl-pptp-vpn}
{:faq}

A **VPN SSL** permite que um usuário crie um túnel seguro da área de trabalho remota para a
{{site.data.keyword.BluSoftlayer_notm}}Rede privada. Ela é compatível com uma variedade de sistemas operacionais.

A **VPN PPTP** permite o mesmo túnel seguro, mas se conecta usando o software de cliente especializado na área de trabalho ou dispositivo dedicado de um usuário. No entanto, o PPTP foi descontinuado. Consulte [Descontinuação da VPN do PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obter mais informações.

## Por que não consigo incluir usuários adicionais para VPN do PPTP?
{:#why-am-i-unable-to-add-users-for-pptp-vpn}
{:faq}

O PPTP foi descontinuado. Consulte [Descontinuação da VPN do PPTP](/docs/infrastructure/iaas-vpn?topic=VPN-pptp-vpn-deprecation) para obter mais informações.

## Quais são as categorias disponíveis para o status de gerenciamento de um usuário da VPN no Portal do cliente?
{:#what-are-available-categories-vpn-management}
{:faq}

As categorias de status do cliente incluem aquelas que podem ser atualizadas por um usuário e aquelas que podem aparecer automaticamente. Eles incluem:

* **Ativo** - o usuário tem acesso ao [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) e à VPN baseada em permissões configuradas pelo administrador de conta. Esse status pode ser selecionado manualmente ou mudado a qualquer momento.
* **Desativado** - o usuário não tem acesso a nenhuma permissão ou assinatura na conta, incluindo [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) e VPN. Se configurado como desativado por outro usuário na conta, esse status pode ser manualmente selecionado e/ou mudado a qualquer momento.
* **VPN Apenas** - o usuário só tem acesso à conectividade de VPN e não pode acessar o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Esse status pode ser selecionado manualmente ou mudado a qualquer momento.
* **Inativo** - o usuário não utilizou o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) ou a VPN nos últimos 60 dias. Esse é um status gerado pelo sistema.
* **cancel_pending** - um administrador na conta cancelou esse usuário e o cancelamento está sendo processado atualmente. Esse status é gerado pelo sistema.

## Como configurar a VPN de SSL?
{:#how-do-i-set-up-ssl-vpn}
{:faq}

Para obter instruções detalhadas, consulte [Conectar-se à VPN SSL - Windows 7 e superior](/docs/infrastructure/iaas-vpn?topic=VPN-connect-ssl-vpn-windows7#connect-ssl-vpn-windows7).



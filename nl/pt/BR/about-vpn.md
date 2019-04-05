---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: VPN access, private network, public access

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sobre a VPN
{:#about-iaas-vpn}

O acesso à VPN permite gerenciar remotamente todos os servidores e serviços associados à sua conta por meio da rede
privada do IBM Cloud. Uma conexão VPN do seu local com a rede privada permite **gerenciamento fora
da banda e resgate de servidor** por meio de um túnel VPN criptografado.

Comunicar-se usando a rede privada é inerentemente mais seguro. Isso fornece flexibilidade para limitar o acesso
público ao mesmo tempo em que ainda permite o gerenciamento de seus servidores. Qualquer usuário em sua conta pode receber acesso à VPN, que está disponível como SSL.
Interações de VPN por meio do [Portal do cliente
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) permitem a
customização do acesso à VPN no nível do usuário.

## Quais são algumas maneiras de usar a VPN SSL?
{:#ways-to-use-iaas-vpn}

Este gateway seguro fora da banda dá acesso ao seu servidor na rede privada. Os usos comuns são:

* Conectar-se ao endereço IP privado do seu servidor (10.x.x.x) para SSH ou RDC.
* Conectar-se à placa IPMI para console remoto/acesso/monitoramento.
* Montar unidades no Windows ou Red Hat de casa ou do PC de trabalho por conveniência.
* Encerrar a interface pública em servidores de banco de dados e gerenciar na rede privada.
* Encerrar a interface pública ao configurar o servidor pela primeira vez.
* Encerrar a interface pública durante atualizações de segurança críticas.
* Encerrar a interface pública durante a violação de segurança e resolver o problema por meio da rede privada.

## Principais Recursos
{:#iaas-vpn-key-features}

 * Nossa rede privada oferece uma maneira gratuita para se comunicar com os servidores e gerenciá-los. A VPN é o gateway para
essa rede privada.
 * Os pontos de acesso em todo o mundo criam os melhores e mais rápidos acesso e interação possíveis. O IBM Cloud atualmente
tem pontos de acesso VPN em muitas cidades.
 * Visite http://www.softlayer.com/vpn-access para uma lista de pontos de acesso VPN à rede privada {{site.data.keyword.BluSoftlayer_notm}}.

## Como ela funciona
{:#iaas-vpn-how-it-works}

Com o acesso à VPN, use o SSL para se conectar com a rede privada e gerenciar seu servidor e serviços. 

## Conexões VPN SSL
{:#iaas-vpn-ssl-vpn-connections}

A VPN SSL é uma conexão de acesso rápido que conecta você à nossa rede privada diretamente de um navegador. A VPN SSL é
compatível com o Windows XP ou mais recente e ActiveX, Fedora, Ubuntu e Mac OSX. O acesso global à nossa rede privada está
disponível em uma única URL, que permite escolher o terminal VPN mais próximo.

## Limite de sub-rede da VPN SSL
{:#iaas-vpn-ssl-vpn-subnet-limit}

O cliente da VPN SSL possui um limite de sub-rede físico de 64 bits que pode ser usado para preencher a sua tabela de
roteamento. Se a sua conta tiver mais de 64 sub-redes, certifique-se de modificar as permissões da VPN SSL para usar sua atribuição de sub-rede manual. Se você não fizer isso, algumas sub-redes poderão ficar inacessíveis por meio da VPN SSL.

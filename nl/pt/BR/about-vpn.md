---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sobre a VPN

O acesso à VPN permite gerenciar remotamente todos os servidores e serviços associados à sua conta por meio da rede
privada do IBM Cloud. Uma conexão de VPN de sua localização para a rede privada permite o gerenciamento fora da banda e o resgate do servidor por
meio de um túnel VPN criptografado.

Comunicar-se usando a rede privada é inerentemente mais seguro. Isso fornece flexibilidade para limitar o acesso
público ao mesmo tempo em que ainda permite o gerenciamento de seus servidores. Qualquer usuário em sua conta pode receber acesso à VPN, que
está disponível como SSL e PPTP. Interações de VPN por meio do [Portal do cliente
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) permitem a
customização do acesso à VPN no nível do usuário.

## Quais são algumas maneiras de usar a VPN SSL?

Este gateway seguro fora da banda dá acesso ao seu servidor na rede privada. Os usos comuns são:

* Conectar-se ao endereço IP privado do seu servidor (10.x.x.x) para SSH ou RDC.
* Conectar-se à placa IPMI para console remoto/acesso/monitoramento.
* Montar unidades no Windows ou Red Hat de casa ou do PC de trabalho por conveniência.
* Encerrar a interface pública em servidores de banco de dados e gerenciar na rede privada.
* Encerrar a interface pública ao configurar o servidor pela primeira vez.
* Encerrar a interface pública durante atualizações de segurança críticas.
* Encerrar a interface pública durante a violação de segurança e resolver o problema por meio da rede privada.

## Recursos-chave

 * Nossa rede privada oferece uma maneira gratuita para se comunicar com os servidores e gerenciá-los. A VPN é o gateway para
essa rede privada.
 * Oferecemos as opções VPN SSL e VPN PPTP.
 * Os pontos de acesso em todo o mundo criam os melhores e mais rápidos acesso e interação possíveis. O IBM Cloud atualmente
tem pontos de acesso VPN em muitas cidades.
 * Visite http://www.softlayer.com/vpn-access para uma lista de pontos de acesso VPN à rede privada {{site.data.keyword.BluSoftlayer_notm}}.

## Como isso funciona

Com o acesso à VPN, há duas maneiras de se conectar com a rede privada e gerenciar seu servidor e serviços. Essas opções
incluem conexões VPN SSL e PPTP. Conecte-se à rede privada usando qualquer método, com base em suas necessidades ou preferências
individuais.
 
## Conexões VPN SSL

A VPN SSL é uma conexão de acesso rápido que conecta você à nossa rede privada diretamente de um navegador. A VPN SSL é
compatível com o Windows XP ou mais recente e ActiveX, Fedora, Ubuntu e Mac OSX. O acesso global à nossa rede privada está
disponível em uma única URL, que permite escolher o terminal VPN mais próximo.

## Limite da sub-rede VPN SSL

O cliente da VPN SSL possui um limite de sub-rede físico de 64 bits que pode ser usado para preencher a sua tabela de
roteamento. Se a sua conta tiver mais de 64 sub-redes, certifique-se de modificar as permissões da VPN SSL para usar sua atribuição de sub-rede manual. Se você não fizer isso, algumas sub-redes poderão ficar inacessíveis por meio da VPN SSL.

## Conexões da VPN PPTP

A VPN PPTP permite que você se conecte à rede privada de forma segura, usando o software cliente específico do SO da sua
área de trabalho ou usando um dispositivo dedicado como um firewall ou roteador. Atualmente fornecemos conectividade de VPN para
Windows XP ou mais recente, Fedora, Ubuntu e Mac OSX. A opção de conexão PPTP é projetada para aqueles que buscam conectar um
escritório inteiro ou que não podem se conectar usando a opção VPN SSL. Conexões PPTP são estabelecidas com um único data center que
pode ser escolhido quando a conexão VPN é configurada.

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: PPTP VPN deprecation, PPTP VPN, IBM Cloud, private network

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Descontinuação da VPN PPTP
{:#pptp-vpn-deprecation}

A VPN PPTP foi descontinuada em 12 de junho de 2018 e não é mais oferecida aos clientes. Agradecemos seu interesse. Para descobrir algumas possíveis alternativas, continue lendo.

## O que é VPN?
{:#pptp-vpn-deprecation-what-is-vpn}
O acesso à VPN permite que os usuários gerenciem todos os servidores remotamente e com segurança na rede privada do IBM Cloud. Uma conexão de VPN de sua localização para a rede privada permite o gerenciamento fora da banda e o resgate do servidor por
meio de um túnel VPN criptografado. Com o acesso de VPN, é possível:

* Estabeleça uma conexão VPN com a rede privada por SSL, **PPTP** ou IPSec
* Acesse seu servidor usando seu endereço IP privado 10.x.x.x por SSH ou RDP
* Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor ou necessidades de resgate adicionais

## Descontinuação do PPTP
{:#pptp-deprecation-vpn}
Como outras opções de VPN se tornaram mais seguras e versáteis, a necessidade do PPTP diminuiu. O
{{site.data.keyword.BluSoftlayer_notm}} fornece diversas outras opções, tais como SSL ou IPSec,
que são mais sofisticadas e protetoras do que o PPTP.

**Por esses motivos, o {{site.data.keyword.BluSoftlayer_notm}} não está mais oferecendo o PPTP desde 12 de junho de 2018.**
{:important}


## Perguntas Freqüentes
{:#pptp-vpn-deprecation-faq}

**P: Por que o PPTP foi descontinuado?**

**R:** Para fornecer a mais alta qualidade de proteção, o {{site.data.keyword.BluSoftlayer_notm}} descontinuou o uso do PPTP. O {{site.data.keyword.BluSoftlayer_notm}} deseja manter a promessa aos nossos clientes de que
a segurança da privacidade e dos dados é de extrema importância. 

**P: Quais outros tipos de acesso VPN estão disponíveis além do PPTP?**

**R:** O {{site.data.keyword.BluSoftlayer_notm}} oferece várias opções que requerem somente uma configuração simples.
  1. A VPN SSL é uma conexão de acesso rápido que conecta você à nossa rede privada diretamente de um navegador. A VPN SSL é
compatível com o Windows XP ou mais recente e ActiveX, Fedora, Ubuntu e Mac OSX. O acesso global à nossa rede privada está
disponível em uma única URL, que permite escolher o terminal VPN mais próximo. Veja [Configurar conexão VPN por SSL](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ssl-vpn-connections) para obter mais detalhes sobre como começar a usar essa opção.
  2. O IPSec é um conjunto de protocolos projetado para autenticar e criptografar todo o tráfego
IP entre dois locais. Ele permite que dados confiáveis passem por redes que, de outra forma, seriam consideradas inseguras. Para obter informações mais gerais relacionadas ao IPSec, consulte [Configurar a VPN por IPSec](/docs/infrastructure/iaas-vpn?topic=VPN-set-up-ipsec-vpn) e os outros [documentos de referência](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation)
para começar a usar esse serviço. 

**P: E se minhas práticas de negócios exigirem PPTP?**

**R:** Estão disponíveis diversas opções caso o PPTP seja requerido para suas
necessidades de negócios. **Nem todas as opções possíveis são abrangidas aqui. Observe que as
opções a seguir requerem configuração completa dos dois terminais. O cliente é responsável pela
configuração dessas opções.**
  1. Virtual Router Appliance. O Virtual Router Appliance, também conhecido como Vyatta, serve
como um gateway e um roteador para o seu ambiente. Ele contém zonas que consistem em sub-redes. As regras
de firewall são definidas entre zonas para comunicação entre si. Para zonas que não precisam se comunicar
com outras, nenhuma regra de firewall é necessária porque todos os pacotes serão descartados. Consulte
[Introdução ao Virtual Router Appliance](/docs/infrastructure/virtual-router-appliance?topic=virtual-router-appliance-getting-started-with-ibm-virtual-router-appliance)
para obter mais detalhes sobre como começar a usar esse serviço. 
  2. Firewall FSA. O FortiGate Security Appliance (FSA) 10 Gbps é um firewall de hardware que pode
ser configurado para proteger o tráfego em múltiplas VLANs para redes públicas e privadas. No Portal do cliente, ele é chamado de “Firewall de múltiplas VLANs”. Consulte [Introdução ao FSA 10 Gbps](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-getting-started-with-fortigate-security-appliance-10gbps) para obter mais detalhes sobre como começar a usar esse serviço. 
 
As opções anteriores são algumas das possibilidades que poderão ser exploradas se o PPTP for requerido para suas necessidades de negócios após o serviço não ser mais fornecido pelo {{site.data.keyword.BluSoftlayer_notm}}. Agradecemos por seus negócios.
{:note}

---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: IPSec VPN, IP address, IP traffic

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configurar a VPN do IPSec
{:#setup-ipsec-vpn}

## O que é a VPN do Internet Protocol Security?
{:#what-is-ipsec-vpn}

Internet Protocol Security é um conjunto de protocolos projetados para autenticar e criptografar todo o tráfego IP entre dois locais, usando um modo de túnel que fornece uma rede criptografada de site para site. Ele permite que dados confiáveis passem pelas redes que, caso contrário, seriam considerados inseguros.   Para obter informações gerais sobre Internet Protocol Security, consulte os [documentos de referência](/docs/infrastructure/iaas-vpn?topic=VPN-external-reference-documentation).


O Acesso à VPN do IBM Cloud permite que os usuários gerenciem todos os servidores remotamente e de forma segura por meio da rede privada do IBM Cloud.  Uma conexão de VPN de sua localização para a rede privada fornece a capacidade de gerenciamento fora da banda e de resgate do servidor por meio de um túnel VPN criptografado.  Com o acesso de VPN, é possível:

   * Estabeleça uma conexão de VPN com a rede privada usando SSL ou IPSEC
   * Acesse o servidor por meio do endereço IP privado 10.x.x.x usando SSH ou RDP
   * Conecte-se ao endereço IP do IPMI do seu servidor para obter gerenciamento do servidor adicional ou necessidades de resgate.

Fornecemos o serviço Internet Protocol Security para clientes para gerenciamento de seus ambientes. Ele não é recomendado para cargas de trabalho de produção.


## Configurando uma conexão de IPSec
{:#setup-ipsec-connection}

### Parâmetros de negociação
{:#setup-ipsec-vpn-negotiation-parameters}
![Parâmetros de negociação](images/IPSec_VPN.png)

Você precisará saber as seguintes informações para o lado remoto da VPN do Internet Protocol Security:
- Endereço IP estático para terminal VPN
- Chave pré-compartilhada (senha)
- Algoritmo de criptografia (DES, 3DES, AES128, AES192, AES256)
- Autenticação (MD5, SHA1, SHA256, para fase 1 e 2)
- Grupo Diffie-Hellman (para fase 1 e 2)
- O Perfect Forward Secrecy (PFS) é usado?
- Tempo de vida da chave (para fase 1 e 2) - **NOTA:** O nosso sistema mede esse valor em segundos!

Assim que você tiver essas informações disponíveis, será possível configurar os parâmetros básicos de negociação da conexão VPN.

### Redes protegidas
{:#setup-ipsec-vpn-protected-networks}

Nas propriedades da conexão VPN, deve-se definir as redes na extremidade remota do túnel, assim como as redes locais para o túnel. Em "Sub-rede protegida do cliente (remoto)", insira o espaço de endereço IP privado em notação CIDR para a extremidade remota (não IBM) do túnel Internet Protocol Security.

<span style="text-decoration: underline">Por exemplo:</span> Se sua rede na extremidade remota do túnel usar uma única sub-rede 10.0.0.0 com uma máscara de rede 255.255.255.0, você digitará Endereço IP 10.0.0.0/CIDR 24 para a seção "Sub-rede protegida de cliente (remoto)".

### Conversão de Endereço de Rede (NAT)
{:#setup-ipsec-vpn-nat}

Com a VPN IPSec, você também tem permissão para definir endereços IP privados na rede {{site.data.keyword.BluSoftlayer_notm}} que roteará o tráfego para sub-redes remotas na outra extremidade da conexão VPN.  Com isso, o tráfego de Internet privado é encaminhado para um dos seus endereços IP internos de uma máquina atrás da sua VPN, sem expor o local remoto para acesso total à Internet.  

### Conversão de endereço de rede/sub-redes de conversão de endereço de rede estática designadas
{:#setup-ipsec-vpn-nat-static-subnets}

Para configurar um IP de VPN remoto com uma entrada de conversão de endereço de rede estática: 

 * Selecione a seta vermelha para exibir a lista de sub-redes na seção **Sub-redes de conversão de endereço de rede estática designadas**. Cada IP na sub-rede será exibido.  
 * Insira o IP na extremidade remota da conexão VPN na coluna **IP do cliente** e insira um nome para o mapeamento sob a coluna **Nome**.  
 * Selecione **Incluir/modificar as conversões de endereço de contexto** e **Aplicar configurações** para salvar e aplicar a configuração.
 
Essa ação configura uma conversão de rede um-para-um estática para o tráfego de retorno, que é usada por seus hosts atrás do concentrador de VPN do IBM Cloud para se comunicar com os hosts atrás do peer da VPN remota. Por exemplo, todo o tráfego para o IP 10.1.255.92 será convertido e encaminhado para o IP 192.168.10.15 do cliente. Esse redirecionamento elimina a necessidade de
entradas de rota adicionais no servidor IBM Cloud.

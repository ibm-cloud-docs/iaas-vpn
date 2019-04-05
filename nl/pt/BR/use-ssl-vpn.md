---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Use SSL VPN Navigate, private IP address, private VLAN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Usar VPN SSL
{:#use-ssl-vpn}

1. Navegue para o link **Login de VPN SSL** no Portal do cliente selecionando **Suporte > Login de VPN SSL** no menu Navegação e, em seguida, insira suas credenciais
2. O túnel VPN SSL será estabelecido quando você observar o "A" em sua barra de tarefas.
3. Parabéns, agora você está em sua VLAN privada.

## Agora eu estou conectado... o que eu faço?
{:#now-im-connected-what-do-i-do}

1. Use SSH ou RDC (serviços de terminal) para se conectar ao endereço IP privado do seu servidor (10.x.x.x) para gerenciamento do servidor.
2. Para usar as funções de console remoto ou reinicialização, conecte-se à sua placa IPMI 2.0 por meio do software SuperMicro; consulte o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) para obter instruções de download.
3. É possível mapear uma unidade para o servidor (Windows) ou montar uma unidade para o servidor (Red Hat).

## Dicas e truques
{:#ssl-vpn-tips-tricks}

1. Seu IP do IPMI e IP privado são separados por um dígito; não os confunda.
2. Não é possível usar SSH ou RDC para se conectar à placa IPMI, deve-se usar o software.
3. O seu IP do IPMI e o IP privado estão localizados em sua seção de hardware em cada **Servidor**.
4. Sua placa IPMI "atende" na interface IP privada e redireciona o tráfego IPMI para a placa IPMI.

## Instruções de IPMI específicas do produto
{:#product-specific-impi-instructions}

* Para obter mais informações sobre como usar o IPMI em um compartilhamento CIFS, consulte [Montando um ISO em um servidor bare metal](/docs/bare-metal?topic=bare-metal-option-1-preferred-using-ipmi-iso-on-a-cifs-share-#option-1-preferred-using-ipmi-iso-on-a-cifs-share-).
* Para obter mais informações sobre como usar o IPMI com VMWare, consulte [Instalando o VMware vSphere ESXi por meio de console remoto e mídia virtual](/docs/infrastructure/vmware?topic=VMware-installing-vsphere-esxi).

* Para obter mais informações sobre como usar o IPMI com o hardware IBM POWER, consulte [Instalando o IPMItool](https://www.ibm.com/support/knowledgecenter/TI0003H/p8eih/p8eih_ipmitool.htm).

**Aviso:**

Se desativar `eth0` (que é a interface de rede privada), você perderá toda a funcionalidade IPMI, incluindo monitoramento, console remoto, reinicialização remota e mais. Se você deseja bloquear o acesso à interface privada, consulte a lista de endereços IP permitidos que podem ser inseridos em suas Tabelas de IP ou Firewall do servidor.

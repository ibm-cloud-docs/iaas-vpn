---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: Linux Fedora, SSL VPN connections Windows, backend IP address

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Configurar conexões de VPN SSL
{:#setup-ssl-vpn-connections}

Windows, Linux Fedora e Linux requerem instruções individualizadas de conexão, que são mostradas neste documento. Aqui estão alguns exemplos de como é possível usar uma conexão VPN SSL:

* Área de trabalho remota para o endereço IP de backend do seu servidor (10.4.X.X) para administração de seus servidores do
Windows 2003.
* SSH para o endereço IP de backend do seu servidor (10.4.X.X) para administrar seus servidores UNIX.
* Use um cliente IPMI para controlar seu servidor usando o endereço IPMI de backend (10.4.X.X). É possível fazer download da ferramenta do cliente IPMI depois que ela está conectada acessando http://downloads.softlayer.local/ipmi/ (deve-se estar conectado à VPN privada do SoftLayer).
  * **Nota:** IPMIView requer Java para ser instalado.  http://www.sun.com/java/
* Testando seu website nas IPs de backend antes de torná-las ativas em seus IPs públicos.
* Transferência de arquivos de dados protegidos entre seus servidores e sua casa/escritório.
* Backup de arquivos de configuração de seus servidores para sua casa/escritório.
* Conecte-se com segurança ao nosso [Portal da web](http://control.softlayer.com/).

## Windows (Internet Explorer)
{:#setup-ssl-vpn-connections-windows}

1. Abra o Internet Explorer e navegue para `http://www.softlayer.com/vpn-access`.
* Depois de ter inserido o seu nome do usuário e a senha, você será solicitado a instalar um plug-in ActiveX. Deve-se instalar esse plug-in para se conectar à sua rede de backend. 
* Também deve-se ter direitos administrativos na sua estação de trabalho para instalar o plug-in ActiveX. Se você não tiver direitos para instalar o plug-in, peça ao seu administrador do sistema local para instalá-lo para você. 
* Quando o plug-in ActiveX estiver instalado, um conector de rede VPN SSL da matriz ativará e estabelecerá uma conexão com o dispositivo VPN. Se bem-sucedido, um '**A**' vermelho aparecerá na barra de tarefas. Você pode clicar no '**A**' a qualquer momento para ver o status de sua conexão VPN SSL: seu status, endereço IP designado, servidores DNS designados, rotas de rede e o tempo conectado. 
* Você pode minimizar sua sessão do navegador a qualquer momento e continuar a usar outros aplicativos com segurança na rede privada. 
* Quando tiver concluído, desconecte selecionando o botão de desconexão à direita ou simplesmente feche a janela.

## Linux Fedora 
{:#setup-ssl-vpn-connections-linux}

O Firefox não suporta mais plug-ins NPAPI (applets java). Use um navegador diferente para executar estas etapas.
{:note}

É recomendado que você execute todos os comandos como raiz. (`setuid root`)

1. Faça download do Java em `http://java.com/en/download/manual.jsp`. Este é um arquivo autoextrator Linux.
* Feche o navegador.
* Mova o arquivo para onde você deseja instalar o Java (geralmente em `/usr/local`)
* Torne o arquivo executável usando o comando `chmod +x jre-6u1-linux-i586.bin`
* Execute o instalador usando o comando `./jre-6u1-linux-i586.bin`
* Concorde com os termos e instale.
* Depois que a instalação for concluída, deve-se criar um symlink.

## Exemplo de Linux
{:#setup-ssl-vpn-connections-linux-example}

1. Abra o navegador e acesse `http://www.softlayer.com/vpn-access`.
* Efetue login com seu nome do usuário e senha do portal do cliente.
* Depois de conectado, selecione a guia **Rede**.
* Um botão de conexão/instalação é exibido. Selecione-o e você receberá uma solicitação para instalar um componente Java.
* Deixe a instalação do componente para o caminho padrão, que você pode ter que criar manualmente. (`/usr/local/array_vpn`)
* Depois que estiver instalado, uma janela deve aparecer informando que você está conectado.
* Esta janela deve permanecer aberta para utilizar o túnel de VPN, mas é possível minimizá-la.
* Para testar a conexão, efetue ping em 10.0.80.11 ou no endereço privado do seu servidor. Se houver uma resposta, você estará conectado com êxito.
* Quando concluir, selecione o botão de desconexão na guia 'Rede' ou feche todas as janelas do navegador.

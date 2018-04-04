---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar conexões VPN SSL

Windows, Linux Fedora e Linux requerem instruções individualizadas de conexão, que são mostradas neste documento. Aqui estão alguns exemplos de como é possível usar uma conexão VPN SSL:

* Área de trabalho remota para o endereço IP de backend do seu servidor (10.4.X.X) para administração de seus servidores do
Windows 2003.
* SSH para o endereço IP de backend do seu servidor (10.4.X.X) para administrar seus servidores UNIX.
* Use um cliente IPMI para controlar seu servidor usando o endereço IPMI de backend (10.4.X.X). É possível fazer download da
ferramenta do cliente IPMI quando conectado acessando http://downloads.service.softlayer.com.
  * **Nota:** IPMIView requer Java para ser instalado. http://www.sun.com/java/
* Testando seu website nas IPs de backend antes de torná-las ativas em seus IPs públicos.
* Transferência de arquivos de dados protegidos entre seus servidores e sua casa/escritório.
* Backup de arquivos de configuração de seus servidores para sua casa/escritório.
* Conecte-se com segurança ao nosso portal da web em http://manage.service.softlayer.com.

## Windows (Internet Explorer)

1. Abra o Internet Explorer e navegue para http://www.softlayer.com/vpn-access.
* Depois de ter inserido o seu nome do usuário e a senha, você será solicitado a instalar um plug-in ActiveX. Deve-se instalar esse plug-in para se conectar à sua rede de backend. 
* Também deve-se ter direitos administrativos na sua estação de trabalho para instalar o plug-in ActiveX. Se você não tiver direitos para instalar o plug-in, peça ao seu administrador do sistema local para instalá-lo para você. 
* Quando o plug-in ActiveX estiver instalado, um conector de rede VPN SSL da matriz ativará e estabelecerá uma conexão com o dispositivo VPN. Se bem-sucedido, um '**A**' vermelho aparecerá na barra de tarefas. Você pode clicar no '**A**' a qualquer momento para ver o status de sua conexão VPN SSL: seu status, endereço IP designado, servidores DNS designados, rotas de rede e o tempo conectado. 
* Você pode minimizar sua sessão do navegador a qualquer momento e continuar a usar outros aplicativos com segurança na rede privada. 
* Quando tiver concluído, desconecte selecionando o botão de desconexão à direita ou simplesmente feche a janela.

## Linux Fedora (FireFox)

É recomendado que você execute todos os comandos como raiz. (`setuid root`)

1. Faça download do Java em `http://java.com/en/download/manual.jsp`. Este é um arquivo autoextrator Linux.
* Feche o FireFox.
* Mova o arquivo para onde você deseja instalar o Java (geralmente em `/usr/local`)
* Torne o arquivo executável usando o comando `chmod +x jre-6u1-linux-i586.bin`
* Execute o instalador usando o comando `./jre-6u1-linux-i586.bin`
* Concorde com os termos e instale.
* Depois que a instalação for concluída, deve-se criar um symlink.

## Exemplo do Linux
```
cd /usr/lib/firefox-1.0.4/plugins/
ln -s /usr/local/jre-6u1/plugin/i386/ns7/libjavaplugin_oji.so .
```

1. Abra o Firefox e acesse `http://www.softlayer.com/vpn-access`.
* Efetue login com seu nome do usuário e senha do portal do cliente.
* Depois de conectado, selecione a guia **Rede**.
* Um botão de conexão/instalação é exibido. Selecione-o e você receberá uma solicitação para instalar um componente Java.
* Deixe a instalação do componente para o caminho padrão, que você pode ter que criar manualmente. (`/usr/local/array_vpn`)
* Depois que estiver instalado, uma janela deve aparecer informando que você está conectado.
* Esta janela deve permanecer aberta para utilizar o túnel de VPN, mas é possível minimizá-la.
* Para testar a conexão, efetue ping em 10.0.80.11 ou no endereço privado do seu servidor. Se houver uma resposta, você estará conectado com êxito.
* Quando concluir, selecione o botão de desconexão na guia 'Rede' ou feche todas as janelas do navegador.

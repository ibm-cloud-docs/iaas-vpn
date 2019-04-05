---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: User Access Control, User Accounts, SSL VPN

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Conectar-se à VPN SSL - Windows 7 e superior
{:#connect-ssl-vpn-windows7}

Para se conectar à VPN SSL {{site.data.keyword.BluSoftlayer_notm}}, pode ser necessário executar algumas etapas em seu computador para assegurar a sua capacidade de conexão.

**1. Desligue o Controle de acesso de usuário (UAC) no painel de controle**

1. Navegue para **Iniciar -> Painel de controle -> Contas do usuário -> Mudar configurações de controle de conta do usuário**
* **Desmarque** a caixa ao lado de **Usar Controle de conta do usuário (UAC) para ajudar a proteger seu computador**.

**2. Ative a conta do administrador**

1. Acesse **Iniciar -> Painel de controle ->Ferramentas administrativas -> Gerenciamento de computadores -> Usuários e grupos locais -> Usuários ->** 
* Clique com o botão direito em usuário **Administrador** e selecione **Propriedades** 
* Desmarque a caixa para **Conta está desativada**.

**3. Execute o Internet Explorer como Administrador antes de se conectar à página da VPN SSL**

1. Clique com o botão direito no ícone Internet Explorer e selecione **Executar como administrador** no menu.

Após a conclusão das etapas anteriores, você poderá efetuar login. 

## Efetuar login
{:#connect-windows-login}

1. Acesse [www.softlayer.com/vpn-access](http://www.softlayer.com/vpn-access) e efetue login usando seu nome do usuário e senha do portal. 
* Certifique-se de verificar se o usuário [tem acesso à VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-activate-or-deactivate-ssl-vpn-access-for-a-user).  
* Além disso, certifique-se de configurar uma senha da VPN. Para fazer isso, atualize sua [Página de perfil do usuário](https://control.softlayer.com/account/user/profile) e preencha a caixa **Senha da VPN**.

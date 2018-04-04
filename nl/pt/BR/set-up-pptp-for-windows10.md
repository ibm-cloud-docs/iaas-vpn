---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuração da VPN PPTP no Windows 10

1. Ative o aplicativo **Configurações** no menu **Iniciar** e clique em
**Rede e Internet**.

2. No lado esquerdo do painel **Rede e Internet**, selecione **VPN** e na
página subsequente, selecione **Incluir uma conexão VPN**.

![Incluir conexão VPN](images/vpn1.png)

3. Na página a seguir você configurará a sua conexão VPN PPTP. Aqui estão as configurações:

 * _Provedor VPN:_ Windows (integrado)
 * _Conexão:_ deve-se fornecer um nome para essa conexão, por exemplo, `MyPPTP`.
 * _nome ou endereço do servidor:_ digite o nome do servidor que você deseja atingir. (Por exemplo,
`pptpvpn.dal01.softlayer.com`)
 * _Tipo de VPN:_ escolha "Protocolo de tunelamento ponto a ponto" (PPTP) *_ Tipo de
conexão:_ escolha "Nome do usuário e senha"
  * Agora digite seu nome do usuário e senha da VPN
  * Verifique todos os dados selecionados novamente e pressione **Salvar**

![Configurações de VPN](images/vpn2.png)

4. Assim que você estiver de volta à página principal da VPN, selecione a conexão `MyPPTP` (que
você criou anteriormente) para ser conectado.

![PPTP da Softlayer](images/vpn3.png)

5. Para usar a Internet enquanto conectado, deve-se desativar o gateway remoto, o que pode ser feito por meio do PowerShell.

 * Abra o PowerShell clicando com o botão direito nele e selecionando **Executar como administrador**
 * Digite os seguintes comandos:
 ```
`Get-VpnConnection`
`Set-VpnConnection -Name "MyPPTP" -SplitTunneling $True`
```

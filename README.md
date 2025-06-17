# 🖥️ Guia Rápido: Criando uma Máquina Virtual no Azure

Este tutorial orienta você na criação de uma máquina virtual com Windows Server 2022 no portal do Azure, ideal para fins educacionais ou testes.

## 📋 Pré-requisitos

- Conta ativa no [Portal do Azure](https://portal.azure.com)
- Assinatura do Azure válida
- Conexão com a internet

---

## 1. Acessando o Portal do Azure

- Acesse o [Portal do Azure](https://portal.azure.com)
- Faça login com suas credenciais

---

## 2. Criando a Máquina Virtual

1. No campo de pesquisa do portal, digite **"Máquinas virtuais"** e selecione a opção correspondente.
2. Clique em **"Criar"** e selecione **"Máquina virtual do Azure"**.
3. Na página de criação, preencha os seguintes campos:

   - **Assinatura**: Escolha sua assinatura ativa.
   - **Grupo de Recursos**: Selecione um grupo existente ou crie um novo.
   - **Nome da Máquina Virtual**: Digite `myVM`.
   - **Região**: Escolha a região desejada.
   - **Imagem**: Selecione **"Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2"**.
   - **Tamanho**: Escolha o tamanho da VM conforme suas necessidades.
   - **Conta de Administrador**:
     - **Nome de usuário**: Digite `azureuser`.
     - **Senha**: Crie uma senha com no mínimo 12 caracteres, incluindo letras maiúsculas, minúsculas, números e caracteres especiais.

4. Em **Regras de porta de entrada**, selecione **"Permitir portas selecionadas"** e marque as opções **RDP (3389)** e **HTTP (80)**.
5. Deixe as configurações padrão para os demais campos e clique em **"Examinar + criar"**.
6. Após a validação, clique em **"Criar"** para iniciar a implantação da VM.

---

## 3. Conectando-se à Máquina Virtual

1. Após a implantação, na página de visão geral da VM, clique em **"Conectar"** e selecione **"RDP"**.
2. Na guia **"Conectar-se ao RDP"**, mantenha as opções padrão e clique em **"Baixar arquivo RDP"**.
3. Abra o arquivo RDP baixado e clique em **"Conectar"**.
4. Na janela de autenticação, clique em **"Mais opções"**, selecione **"Usar uma conta diferente"** e insira:
   - **Nome de usuário**: `localhost\azureuser`
   - **Senha**: A senha criada anteriormente.
5. Clique em **"OK"** e, se solicitado, confirme a conexão.

---

## 4. Instalando o Servidor Web (IIS)

1. Na VM, abra o **PowerShell** como administrador.
2. Execute o seguinte comando para instalar o IIS:

   powershell
   Install-WindowsFeature -name Web-Server -IncludeManagementTools

---

## 5. Verificando a Instalação do IIS

1. No portal do Azure, na página de visão geral da VM, copie o Endereço IP público.
2. Cole o IP copiado em um navegador web.
3. Se tudo estiver correto, a página de boas-vindas do IIS será exibida.

---

## 6. Limpando os Recursos

1. Para evitar custos adicionais, exclua os recursos quando não forem mais necessários:
2. Na página de visão geral da VM, clique em "Grupo de recursos".
3. Clique em "Excluir grupo de recursos" na parte superior da página.
4. Digite o nome do grupo de recursos para confirmar e clique em "Excluir".


🔗 Referências:

[Início Rápido: Criar uma máquina virtual do Windows no Portal do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
[Documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/?product=popular)


## Contato
Se tiver dúvidas ou sugestões, entre em contato:
- GitHub: [JulianoTurra](https://github.com/JulianoTurra)


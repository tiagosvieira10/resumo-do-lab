# Como Criar uma Máquina Virtual na Azure

Este guia resume o processo de criação de uma **Máquina Virtual (VM)** na plataforma Microsoft Azure, com foco em iniciantes.

## 🛠️ Passo a Passo

### 1. Acessar o Portal Azure
- Acesse o portal da Azure
- Faça login

### 2. Criar um Novo Recurso
- No menu lateral, clique em **"Criar um recurso"**
- Em seguida, selecione **"Máquina Virtual"**

### 3. Configurar a VM
- **Assinatura**: escolha a conta que será usada para cobrança
- **Grupo de Recursos**: crie um novo ou use um existente
- **Nome da VM**: defina um nome amigável
- **Região**: escolha a localização do data center (ex: "Brazil South")
- **Imagem**: escolha o sistema operacional (ex: Windows 11, Ubuntu 22.04)
- **Tamanho**: selecione o tipo de máquina (ex: B1s, D2s_v3, etc.)
- **Usuário e senha/SSH**: defina as credenciais de acesso

### 4. Configurar Regras de Acesso (Rede)
- Permita o tráfego necessário, como:
  - **RDP** (porta 3389) para Windows
  - **SSH** (porta 22) para Linux
- Opcional: configurar grupo de segurança de rede (NSG)

### 5. Revisar e Criar
- Revise todas as configurações
- Clique em **"Criar"** e aguarde a implantação da máquina virtual

### 6. Acessar a VM
- Após criada, vá em **"Máquinas Virtuais" > [nome da sua VM]**
- Clique em **"Conectar"**
  - Para Windows: via RDP
  - Para Linux: via SSH

---

## 📌 Dicas
- Utilize o plano gratuito se estiver começando
- Lembre-se de parar ou excluir a VM quando não estiver em uso para evitar cobranças
- É possível automatizar esse processo com scripts usando **Azure CLI** ou **ARM templates**

 
  

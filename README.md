# Configuração de Instância de Banco de Dados na Azure

Este é um resumo do que aprendi sobre a criação e configuração de uma instância de banco de dados na plataforma Microsoft Azure. O foco foi entender o processo de provisionamento, escolha de recursos e acesso ao banco.

## Conceitos Aprendidos

### 1. Tipos de Banco de Dados Suportados
- Azure SQL Database (banco relacional gerenciado)
- Azure Database for MySQL
- Azure Database for PostgreSQL
- Cosmos DB (NoSQL)

### 2. Criando uma Instância
- Acesso pelo portal: **Criar recurso > Banco de dados > [Tipo desejado]**
- Seleção da **assinatura** e **grupo de recursos**
- Definição do **nome do servidor** e **nome do banco**
- Escolha da **versão do banco de dados**
- Autenticação via **login e senha de administrador**

### 3. Configurações Importantes
- **Camada de preço (Pricing Tier)**: escolha entre níveis como Basic, Standard ou Premium, com base em desempenho e capacidade
- **Região**: define onde a instância será hospedada (impacta na latência)
- **Backup e redundância**: configurações de alta disponibilidade e recuperação

### 4. Configuração de Acesso
- **Configuração de firewall**: liberar IPs que podem acessar a instância
- **Strings de conexão**: disponíveis no painel da instância, prontos para uso em aplicações

### 5. Acesso e Teste
- Conexão via ferramentas como:
  - Azure Data Studio
  - SQL Server Management Studio (SSMS)
  - MySQL Workbench, psql, entre outros
- Teste de conexão utilizando a string fornecida no portal

---

## Observações Finais
- A Azure gerencia automaticamente atualizações e backups dependendo da configuração escolhida
- Ideal para aplicações que precisam de alta disponibilidade e escalabilidade
- É possível automatizar o provisionamento usando **Azure CLI**, **ARM Templates** ou **Terraform**

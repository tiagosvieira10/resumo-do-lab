# Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

Este resumo registra os principais aprendizados sobre como configurar e dimensionar recursos em Máquinas Virtuais (VMs) na Microsoft Azure. O foco foi entender como escolher corretamente os tamanhos de VM, ajustar desempenho e gerenciar recursos de forma eficiente e escalável.

## Conceitos Aprendidos

### 1. Escolha do Tamanho da VM
- Azure oferece diferentes **SKUs** (tipos e tamanhos de VM), divididos por famílias:
  - **B-series**: econômicas, para cargas intermitentes
  - **D-series**: uso geral
  - **E-series**: otimizadas para memória
  - **F-series**: otimizadas para CPU
  - **NV/NC-series**: com suporte a GPU
- Cada SKU define:
  - Número de vCPUs
  - Memória RAM
  - Armazenamento temporário
  - Capacidade de rede

### 2. Configurações de Disco
- Tipos de disco:
  - **Disco do SO (geralmente SSD premium ou padrão)**
  - **Disco de dados adicionais** (para armazenamento de arquivos, banco, etc.)
- Escolha entre discos:
  - **Standard HDD**: baixo custo
  - **Standard SSD**: equilíbrio entre custo e desempenho
  - **Premium SSD**: alta performance

### 3. Autoescalabilidade (Auto-Scale)
- Implementação de regras para escalar automaticamente:
  - Baseado em CPU, memória, tempo de resposta ou outras métricas
  - Ideal para ambientes com variação de carga (ex: aplicações web)
- Possível via:
  - **Virtual Machine Scale Sets**
  - **Azure Monitor + Alertas + Ações**

### 4. Monitoramento e Performance
- Uso de ferramentas como:
  - **Azure Monitor**
  - **Log Analytics**
  - **Metrics e Insights de VM**
- Identificação de gargalos e ajuste de recursos com base no uso real

### 5. Otimização de Custos
- Reduzir recursos quando o uso é baixo (ex: desligar VMs fora do horário comercial)
- Escolher SKUs com bom custo-benefício
- Utilizar **reservas de instância** (1 ou 3 anos) para economizar

---

## Boas Práticas
- Sempre revisar as métricas antes de mudar o tamanho da VM
- Testar diferentes tamanhos em ambiente de desenvolvimento
- Usar **tags** para organização e controle de custos por equipe ou projeto
- Separar discos de dados do disco do sistema operacional

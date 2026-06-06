# Análise de Telecomunicações — Decomposição do Projeto CallMeMaybe  
## Exploração, Estatística Descritiva, KPIs e Plano de Ação

## Objetivo do Projeto
O objetivo deste projeto é analisar dados de telecomunicações para compreender o comportamento dos usuários, identificar padrões de uso e avaliar a eficiência operacional do serviço.  
A partir da exploração, limpeza e análise estatística dos dados, buscamos revelar:

- tendências temporais,  
- diferenças entre planos tarifários,  
- sazonalidades,  
- anomalias e outliers,  
- perfis de uso por cliente,  
- e impactos operacionais relevantes.

Esses insights servem como base para definição de KPIs, construção de visualizações e recomendações estratégicas.

---

## Análise Estatística Descritiva

A análise inicial revelou forte **assimetria** nas variáveis relacionadas a chamadas:

- `call_duration` e `total_call_duration` apresentam valores máximos extremamente elevados (≈ 40h e 46h).  
- `calls_count` possui grande dispersão, chegando a **4.817 chamadas** em um único registro.  
- `operator_id` e `user_id` apresentam comportamento consistente com identificadores numéricos.

**Conclusão:**  
Há presença clara de **outliers** e possíveis inconsistências operacionais.  
Esses pontos exigem tratamento antes das análises finais.

---

## Diferenças Entre Planos Tarifários

A média de chamadas por cliente varia significativamente entre os planos:

| Plano | Média de Chamadas |
|-------|-------------------|
| **A** | **438** |
| **B** | **169** |
| **C** | **124** |

A diferença é grande e consistente.

**Conclusão estatística:**  
Rejeitamos H₀ e aceitamos H₁.  
Os planos tarifários **influenciam significativamente** o uso do serviço.

---

## KPIs Selecionados

Os KPIs foram definidos para fornecer uma visão clara e estratégica sobre:

- **qualidade operacional**,  
- **engajamento dos clientes**,  
- **desempenho dos planos tarifários**,  
- **comportamento de heavy users**,  
- **distribuição de chamadas**,  
- **impacto de outliers**.

Esses indicadores são essenciais para validar hipóteses e orientar decisões de negócio baseadas em evidências.

---

## Distribuição de Chamadas e Heavy Users

A distribuição de chamadas apresenta uma **cauda longa**:

- A maioria dos clientes realiza poucas chamadas.  
- Uma minoria concentra volumes extremamente altos.  
- Heavy users representam grande parte do consumo total.

Esse padrão é típico em serviços de telecom e reforça a importância de segmentar clientes por perfil de uso.

---

## Comparação Entre Planos Tarifários

A análise dos KPIs confirma diferenças claras entre os planos:

- **Plano A**: menor base de clientes, porém usuários com uso muito intenso.  
- **Plano B**: comportamento intermediário, mas com heavy users próximos ao Plano C.  
- **Plano C**: maior base de clientes, porém menor volume médio de chamadas.

**Conclusão:**  
Os planos atraem **perfis distintos de utilização**, validando a hipótese inicial.

---

## Plano de Ação — Otimização dos Planos Tarifários

### **1. Fortalecer o Plano B como opção intermediária**
O Plano B apresenta uso mais intenso do que o esperado para sua base reduzida.  
Pode ser reposicionado como alternativa para usuários do Plano C com tendência de crescimento.

### **2. Criar incentivos de migração do Plano C → Plano B**
O Plano C concentra muitos usuários leves, mas também heavy users relevantes.  
Benefícios moderados (minutos extras, vantagens de preço, serviços adicionais) podem estimular a migração.

### **3. Manter atenção especial aos heavy users do Plano A**
Apesar da base pequena, esses clientes concentram grande parte do uso total.  
Ações de retenção e benefícios exclusivos podem reduzir churn e preservar receita.

### **4. Monitorar evolução do consumo no Plano C**
A cauda longa indica que alguns usuários podem ultrapassar o perfil do plano.  
Monitoramento contínuo permite identificar momentos ideais para upgrades.

---

## Tecnologias Utilizadas
- Python (exploração, limpeza e análise estatística)  
- Pandas / NumPy  
- Visualização (Seaborn / Matplotlib)  
- Jupyter Notebook  

---

## Estrutura do Repositório

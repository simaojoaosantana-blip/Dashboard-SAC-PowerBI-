# 📞 Dashboard SAC — Análise de Chamados de Suporte

**Dashboard interativo em Power BI** analisando ~12k chamados de suporte (2017-2019) para identificar padrões, gargalos e oportunidades de melhoria no atendimento.

**Stack:** Power BI | Excel | Base de dados relacional (Usuarios, Suporte, Problemas, Ocorrências)

---

## 📊 Visão Geral dos Dados

| Métrica | Valor |
|---------|-------|
| **Total de Chamados** | 11,999 |
| **Período** | Jan/2017 — Dez/2019 |
| **Base de Usuários** | 450 usuários |
| **Agentes de Suporte** | 44 analistas |
| **Tipos de Problema** | 21 categorias |
| **Taxa de Resolução** | 72.9% (8,743 encerrados) |

---

## 🎯 Análises Principais

### **1️⃣ Distribuição por Status**

```
Encerrado ........................ 8,743 (72.9%)
Cancelado ........................ 2,323 (19.4%)
Aguardando resposta usuário ...... 933   (7.8%)
```

**Insight:** Mais de 72% dos chamados são resolvidos, indicando boa eficiência. Porém, 19.4% cancelados merece investigação — pode indicar falta de engajamento do usuário ou atendimento inadequado.

---

### **2️⃣ Problemas Mais Frequentes**

| Problema | Ocorrências | % |
|----------|------------|-------|
| Recursos não disponíveis | 1,322 | 11.0% |
| Emitir certificado | 1,253 | 10.4% |
| Conexão lenta | 1,191 | 9.9% |
| Dúvidas/Outros | 955 | 8.0% |
| Página indisponível | 891 | 7.4% |
| Tempo de resposta | 890 | 7.4% |
| Sugestões/Outros | 741 | 6.2% |

**Insight:** Os 3 problemas mais comuns (Recursos, Certificado, Conexão) representam **31.3%** de todos os chamados. Otimizar esses 3 itens reduziria significativamente o volume.

**Recomendação:** 
- Criar FAQ dedicada para "Emitir certificado"
- Investigar infra de "Conexão lenta" (problema técnico)
- Melhorar disponibilidade de "Recursos"

---

### **3️⃣ Performance dos Analistas**

| Analista | Chamados Atendidos | % do Total |
|----------|-------------------|-----------|
| Bruna Serva | 164 | 1.4% |
| Jeferson Pinheiro Mariano | 164 | 1.4% |
| Eric Amante | 149 | 1.2% |
| Matheus Rubio | 148 | 1.2% |
| Gabriel Viana | 142 | 1.2% |

**Insight:** A carga de trabalho está **bem distribuída** entre os 44 analistas (média ~273 chamados por pessoa). Não há gargalos individuais visíveis — o problema é coletivo (volume), não pessoal.

---

### **4️⃣ Evolução Temporal (Chamados por Ano)**

| Ano | Total de Chamados |
|-----|-----------------|
| 2017 | 4,000 |
| 2018 | 3,936 |
| 2019 | 4,063 |

**Insight:** Volume **estável** ao longo do período (~4k chamados/ano). Sem crescimento exponencial — indica que processos e equipe estão em equilíbrio, mas sem capacidade extra para expansão.

---

## 💡 Insights Principais

✅ **Taxa de resolução saudável (72.9%)** — a maioria dos chamados termina com sucesso

✅ **3 problemas representam 31% do volume** — otimizá-los traria ROI imediato

✅ **Distribuição de carga equilibrada** — nenhum analista é gargalo

✅ **Volume estável** — indicativo de serviço consolidado, sem crescimento acelerado

⚠️ **19.4% cancelados** — investigar motivo (usuário desistiu? Problema resolvido outro canal?)

---

## ⚠️ Limitações e Considerações

📌 **Período de 3 anos** (2017-2019) — pode haver mudanças operacionais não refletidas aqui

📌 **"Tempo de Resposta"** registrado (00:04:14 etc) — não há métrica de "Tempo de Resolução", que seria mais relevante

📌 **Problemas categorizados com "Dúvidas/Outros"** (8%) — falta granularidade; recomenda-se subcategorizar

📌 **Falta contexto de satisfação** — não temos NPS ou pesquisa de satisfação para validar qualidade real

---

## 📁 Estrutura do Projeto

```
Dashboard_SAC/
├── Base_SAC.xlsx               # Arquivo Excel com 4 abas
│   ├── dUsuario               # 450 usuários (ID, Nome, Sexo, Datas)
│   ├── dSuporte               # 44 agentes de suporte
│   ├── dProblema              # 21 tipos de problema
│   └── fOcorrencias           # 11,999 chamados (fatos)
├── Dashboard_SAC.pbix          # Arquivo Power BI (visualizações)
└── README.md                   # Este arquivo
```

---

## 🎨 Visualizações do Dashboard

O dashboard Power BI contém:

1. **KPI Cards** — Total de chamados, Taxa de resolução, % Cancelados
2. **Gráfico de Status** — Distribuição por Encerrado/Cancelado/Aguardando (pizza ou colunas)
3. **Top Problemas** — Ranking dos 10 problemas mais comuns (barras horizontais)
4. **Performance por Analista** — Volume atendido (colunas ou tabela)
5. **Timeline Mensal** — Evolução de chamados ao longo do tempo (linha)
6. **Heatmap por Problema × Status** — Qual problema costuma ser cancelado/resolvido

---

## 🔍 Recomendações Baseadas nos Dados

### **Curto Prazo (1-2 meses)**
1. Criar FAQ/Tutorial para "Emitir Certificado" (10.4% dos chamados)
2. Investigar casos de "Cancelamento" — entrevistar usuários
3. Publicar guia "Otimizando Conexão" no portal

### **Médio Prazo (3-6 meses)**
4. Avaliar infraestrutura de "Conexão lenta" com time técnico
5. Melhorar disponibilidade de "Recursos não disponíveis"
6. Implementar chatbot para problemas simples (FAQ, Certificado)

### **Longo Prazo (6-12 meses)**
7. Adicionar pesquisa de satisfação (NPS) para validar qualidade
8. Implementar sistema de categorização mais granular (subcategorias)
9. Automatizar resoluções de problemas recorrentes

---

## 📊 Métricas Monitoradas

| Métrica | Alvo | Status Atual |
|---------|------|------------|
| **Taxa de Resolução** | ≥75% | 72.9% ⚠️ (perto) |
| **% Cancelados** | ≤10% | 19.4% ❌ (acima) |
| **Tempo médio de resposta** | ≤4h | *não monitorado* |
| **Volume por analista** | ≤300/ano | 273 média ✅ |

---

## 🛠️ Como Usar

1. **Abra** `Dashboard_SAC.pbix` no Power BI Desktop
2. **Filtre** por período, problema, ou analista conforme necessário
3. **Exporte** dados para apresentações ou análises complementares
4. **Atualize** a conexão com a fonte de dados (Excel ou banco)

---

## 📈 Próximos Passos

- [ ] Adicionar métrica de "Tempo de Resolução" (não só resposta)
- [ ] Implementar dashboard de "Satisfação do Cliente" (NPS/CSAT)
- [ ] Criar alertas automáticos para taxa de cancelamento > 20%
- [ ] Segmentar análise por "Tipo de Usuário" (novo vs recorrente)
- [ ] Comparar performance mensal com metas de SLA

---

## 📚 Referências

- **Fonte de dados:** Base_SAC.xlsx (11,999 registros)
- **Período:** 2017-2019
- **Responsável pela análise:** [Seu Nome]
- **Data da análise:** Junho 2026

---

*Dashboard desenvolvido para análise de KPIs de Suporte | Julho 2026*

**Tags:** #PowerBI #Analytics #SAC #CustomerSupport #KPI #DataVisualization

# 📊 Mini Projeto — Análise de Campanha de Marketing

Projeto de análise de dados desenvolvido durante o curso **Microsoft Power BI Para Business Intelligence e Data Science** da **Data Science Academy**.

## 🛠️ Ferramentas Utilizadas
- Microsoft Power BI
- Power Query (ETL)
- DAX (Data Analysis Expressions)
- CSV como fonte de dados

## 📁 Fonte de Dados
Base com **2.000 clientes** contendo informações de perfil, comportamento de compra e resposta a campanhas de marketing em 7 países: Brasil, Estados Unidos, Espanha, Chile, Argentina, Alemanha e Portugal.

## 🧹 Etapa 1 — Tratamento dos Dados (Power Query)
- Substituição de valores na coluna **Comprou**: 0 → "Não" e 1 → "Sim"
- Ajuste de tipos de dados por coluna
- Detecção e remoção de outliers via gráfico de dispersão

## 🧮 Etapa 2 — Modelagem e DAX
Criação de medida **Gasto Total** com SUMX agregando 6 categorias de gastos:
```dax
Gasto Total = SUMX(dados_marketing,
    dados_marketing[Gasto com Eletronicos] +
    dados_marketing[Gasto com Brinquedos] +
    dados_marketing[Gasto com Moveis] +
    dados_marketing[Gasto com Utilidades] +
    dados_marketing[Gasto com Alimentos] +
    dados_marketing[Gasto com Vestuario])
```

## 📊 Etapa 3 — Dashboards (4 páginas)

### Visão Cliente
- KPIs: total de clientes, média salarial, compras por canal
- Distribuição por escolaridade e estado civil
- Segmentação por país

### Visão Comportamento
- Gráfico de dispersão: Gasto com Alimentos x Salário Anual
- Árvore hierárquica com drill down: Total Gasto por Estado Civil e Escolaridade
- Total Gasto por número de filhos e adolescentes em casa

### Visão Campanhas
- Taxa de conversão pós-campanha
- Média salarial: convertidos vs não convertidos
- Matriz: Estado Civil x Escolaridade com total de compras
- Clientes convertidos por número de filhos

### Visão Pontos de Venda
- Total de gastos por categoria e país
- Evolução do gasto total por ano e país (2018–2023)
- Segmentação interativa por país

## 💡 Principais Insights
- Taxa de conversão de apenas **16%** — oportunidade de melhoria nas campanhas
- Clientes convertidos têm salário médio **15% maior** ($59 Mil vs $51 Mil)
- **Solteiros sem filhos** são o perfil com maior conversão e gasto
- **Loja física** lidera em volume de compras com 807 transações
- **Estados Unidos** concentra o maior volume de gastos entre os países
- Clientes com **Curso Superior** representam o maior segmento em gasto total

## 📚 Conceitos Aprendidos
- Diferença entre coluna calculada e medida no DAX
- Função SUMX para iteração linha a linha
- Árvore hierárquica com drill down
- Matriz para cruzamento de dados categóricos
- Gráfico de dispersão para identificação de outliers
- Desvio padrão como critério estatístico para outliers
- Taxa de conversão e análise de campanhas de marketing

## 📌 Projetos do Curso
- [x] **1. Marketing** ← atual
- [ ] 2. Comercial
- [ ] 3. Recursos Humanos
- [ ] 4. Logística
- [ ] 5. Financeiro
- [ ] 6. Contábil
- [ ] 7. Mercado de Ações

## 👤 Autor
**Caio Cesar Silva e Souza**
Analista de Dados em formação | Excel • Power Query • Power BI • SQL
[LinkedIn](https://linkedin.com/in/cacesouza)

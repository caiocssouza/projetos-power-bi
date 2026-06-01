# 📊 Dashboard de Análise Financeira

<img width="946" height="527" alt="image" src="https://github.com/user-attachments/assets/291bebf7-9320-41aa-a973-8eed44971ebc" />


Dashboard desenvolvido respondendo perguntas de negócio reais, uma por uma — como acontece no mundo real.

## ❓ Perguntas que guiaram o projeto

1. Qual o Total de Receitas?
2. Qual o Total de Despesas?
3. Qual a Margem de Lucro?
4. Quais componentes geram mais Receita?
5. Quais despesas estão acima ou abaixo da média?
6. Como se comportam Receitas e Despesas por Componente e por Ano?

## 📈 Resultados

| Métrica | Valor |
|---|---|
| Receita Total | R$ 1.920.089 |
| Despesas | R$ 1.152.917 |
| Lucro | R$ 767.172 |
| Margem de Lucro | 39,96% |

## 🛠️ O que foi aplicado

- **ETL no Power Query:** transformação de colunas de datas em linhas com `Table.UnpivotOtherColumns`
- **Medidas DAX:**
```DAX
Receitas = CALCULATE(SUM(DadosFinanceiros[Valor]), Tipo = "Receitas")
Despesas = CALCULATE(SUM(DadosFinanceiros[Valor]), Tipo = "Despesas")
Lucro = [Receitas] - [Despesas]
Margem de Lucro = DIVIDE([Lucro], [Receitas])
```
- **Linha de média** no gráfico de barras para identificar despesas acima e abaixo da média
- **Hierarquia Tipo/Componente** com drill-down por ano
- **Formatação de cartões:** valores completos sem abreviação

## 💡 Aprendizado além da técnica

Nem sempre o visual mais complexo é o melhor. Optei por uma análise descritiva no lugar do gráfico de Principais Influenciadores — o dashboard ficou mais limpo e objetivo.

[LinkedIn](https://linkedin.com/in/cacesouza)

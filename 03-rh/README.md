
# 📊 Projeto 3 — Análise de Recursos Humanos

Projeto desenvolvido durante o curso **Microsoft Power BI Para Business Intelligence e Data Science** da **Data Science Academy**.

## 🛠️ Ferramentas Utilizadas
- Microsoft Power BI
- Power Query (ETL)
- DAX (Data Analysis Expressions)

## 📁 Fonte de Dados
Base com **1.400 funcionários** contendo informações de perfil, gênero, salário, departamento, função, disponibilidade para hora extra e índice de envolvimento no trabalho.

## 🧮 Medidas DAX Criadas

```dax
TotalFuncionarios = COUNTROWS(DatasetRH)
TotalFeminino = CALCULATE([TotalFuncionarios], DatasetRH[Genero] = "Feminino")
%Feminino = DIVIDE([TotalFeminino], [TotalFuncionarios], 0)
TotalMasculino = CALCULATE([TotalFuncionarios], DatasetRH[Genero] = "Masculino")
%Masculino = DIVIDE([TotalMasculino], [TotalFuncionarios], 0)
MediaSalarial = AVERAGE(DatasetRH[Salario_Mensal])
TotalHoraExtra = CALCULATE([TotalFuncionarios], DatasetRH[Disponivel_Hora_Extra] = "Sim")
%HoraExtra = DIVIDE([TotalHoraExtra], [TotalFuncionarios], 0)
```
<img width="955" height="526" alt="Captura de tela 2026-05-07 024125" src="https://github.com/user-attachments/assets/15338b9a-e992-417a-ac05-cdc209eb565d" />

## 💡 Principais Insights
- **1.400 funcionários** no total — 59,86% masculino e 40,14% feminino
- **Média salarial** de R$ 6.927,51
- **71,57%** dos funcionários disponíveis para hora extra
- **Cientista de Dados** é a função com maior número de profissionais
- **59%** dos funcionários têm índice de envolvimento **Bom** no trabalho

## 📊 Visuais Utilizados
- Cards com KPIs
- Gráfico de barras por função
- Gráfico de pizza (hora extra)
- Gráfico de rosca (envolvimento no trabalho)
- Slicer de idade

## 📌 Projetos do Curso
1. Marketing ✅
2. Comercial ✅
3. **Recursos Humanos** ← atual
4. Logística
5. Financeiro
6. Contábil
7. Mercado de Ações

## 👤 Autor
**Caio Cesar Silva e Souza**
Analista de Dados em formação | Excel • Power Query • Power BI • SQL
[LinkedIn](https://linkedin.com/in/cacesouza)

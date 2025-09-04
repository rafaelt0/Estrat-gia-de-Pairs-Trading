# 📊 Backtest de Pairs Trading na B3

---

## 📝 Descrição

Este repositório contém um **pipeline completo de Pairs Trading** utilizando dados da B3, implementado em **Python** com suporte a **SQLite** e **vectorbt**.  

O fluxo do projeto inclui:

1. Criação e manutenção de um banco de dados SQLite com preços e volumes (`ativos_b3.db`)  
2. Download e armazenamento de dados históricos via `yfinance`  
3. Carregamento de tickers com filtro de **volume mínimo**  
4. Seleção de pares cointegrados usando **ADF e KPSS**  
5. Cálculo do **spread** e **z-score exponencial (EWM)**  
6. Geração de sinais de **entrada/saída long/short**  
7. Backtest diário com **portfolio ponderado por volatilidade**  
8. Validação **walk-forward** para reduzir overfitting  

---

## ⚙️ Objetivos

- Manter um banco de dados atualizado com preços, volumes e retornos da B3  
- Selecionar pares com **cointegração estável** e **meia-vida adequada**  
- Testar estratégias **long-short baseadas em z-score**  
- Avaliar a performance do portfólio (**Retorno**, **Sharpe ajustado pelo CDI**)  
- Garantir **validação fora da amostra** usando walk-forward  

---
## 📊 Resultados do Backtest Anual

A estratégia de **Pairs Trading** foi testada de 2020 a 2024. Os resultados demonstram seu desempenho frente à renda fixa (CDI) e ao índice Bovespa (Ibovespa):

| Ano  | Retorno Estratégia (%) | Sharpe | CDI (%) | Ibovespa (%) |
|------|----------------------|--------|---------|--------------|
| 2020 | 24.45                | 1.24   | 2.75    | -1.99        |
| 2021 | 16.41                | 1.11   | 2.65    | 2.92         |
| 2022 | -0.90                | -1.23  | 9.90    | 4.08         |
| 2023 | 28.97                | 1.69   | 5.80    | 13.30        |
| 2024 | 3.00                 | -0.70  | 6.20    | 1.50         |

### 🔹 Observações
- A estratégia apresentou **bons retornos e Sharpe positivos** em 2020, 2021 e 2023, superando CDI e Ibovespa.  
- Em 2022 e 2024, o retorno foi baixo ou negativo, indicando que a estratégia é sensível a **mercados com forte tendência ou choques de volatilidade**.  
- A análise reforça a importância de **monitoramento contínuo dos pares, hedge dinâmico e ajuste anual do portfólio**.






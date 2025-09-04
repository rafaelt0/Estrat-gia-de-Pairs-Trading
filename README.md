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
## 📊 Resultados do Backtest Anual (2020–2024)

A estratégia de **Pairs Trading** foi testada de 2020 a 2024, com os seguintes resultados:

| Ano  | Retorno Estratégia (%) | Sharpe | CDI Acumulado (%) | Retorno Ibovespa (%) |
|------|------------------------|--------|-------------------|----------------------|
| 2020 | 24.45                  | 1.24   | 2.77              | 2.92                 |
| 2021 | 16.41                  | 1.11   | 4.40              | -11.93               |
| 2022 | -0.90                  | -1.23  | 12.39             | 4.69                 |
| 2023 | 28.97                  | 1.69   | 13.04             | 22.28                |
| 2024 | 3.00                   | -0.70  | 10.88             | -10.36               |

> **Fontes**:  
> - CDI Acumulado: [brasilindicadores.com.br](https://brasilindicadores.com.br/cdi/)  
> - Retorno Ibovespa: [sistemaswebb3-listados.b3.com.br](https://sistemaswebb3-listados.b3.com.br/indexStatisticsPage/variation/IBOVESPA?language=pt-br)

---

### 🔹 Análise Comparativa

- **2020**: A estratégia superou o CDI e o Ibovespa, com retorno expressivo de 24.45% e Sharpe de 1.24, indicando boa relação risco-retorno.

- **2021**: Apesar do bom retorno absoluto (16.41%), o Ibovespa teve desempenho negativo (-11.93%), destacando a resiliência da estratégia em mercados voláteis.

- **2022**: Retorno negativo da estratégia (-0.90%), inferior ao CDI (12.39%) e ao Ibovespa (4.69%), sugerindo que a estratégia é sensível a choques de mercado.

- **2023**: Excelente desempenho (28.97%), superando CDI (13.04%) e Ibovespa (22.28%), com Sharpe elevado (1.69), indicando eficiência na captura de oportunidades.

- **2024**: Retorno modesto (3.00%) e Sharpe negativo (-0.70), inferior ao CDI (10.88%) e ao Ibovespa (-10.36%), sugerindo necessidade de reavaliação dos pares ou ajustes na estratégia.

---

Se desejar, posso fornecer gráficos comparativos do equity da estratégia versus CDI e Ibovespa para uma análise visual mais aprofundada. Gostaria de prosseguir com isso?






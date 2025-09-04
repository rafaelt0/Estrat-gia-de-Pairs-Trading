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





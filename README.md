# modelo-precificacao-imobiliaria-avm

# 🏠 Inteligência Imobiliária: Modelo de Precificação Automática (AVM)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Este é um projeto prático de **Inteligência Imobiliária** focado no desenvolvimento de um **AVM (Automated Valuation Model)** para estimar o preço anunciado de imóveis com base em suas características estruturais e localização geográfica.

O projeto simula a realidade de fundos de investimento imobiliário (FIIs) e plataformas de tecnologia do setor (Proptechs), que necessitam de avaliações rápidas e precisas de ativos para tomada de decisão financeira.

---

## 📊 Estrutura do Projeto

O pipeline de dados foi desenvolvido de forma modular no Google Colab e está dividido em três etapas principais:

1. **Engenharia de Features e Tratamento de Outliers:**
   * Cálculo da idade física do imóvel e do preço por $m^2$ de forma automática.
   * Filtro estatístico robusto utilizando o método **IQR (Interquartile Range)** para eliminar distorções e anúncios discrepantes do mercado imobiliário brasileiro.
   * Análise de correlação multivariada via heatmap.

2. **Preparação de Dados e Baseline (Regressão Linear):**
   * Codificação de variáveis categóricas (bairros) usando *One-Hot Encoding*.
   * Divisão estratificada em 80% treino e 20% teste.
   * Ajuste do modelo clássico de Regressão Linear.

3. **Modelagem Avançada e Seleção de Campeão (Random Forest):**
   * Treinamento de um algoritmo de Ensemble (*Random Forest Regressor*).
   * Comparação lado a lado das métricas técnicas e de negócios ($R^2$, MAE e MAPE).
   * Geração de gráfico comparativo de Preço Real vs. Preço Previsto.

---

## 📈 Resultados Obtidos

Após o tratamento de anomalias no mercado imobiliário simulado, os modelos apresentaram a seguinte performance na base de teste:

| Métrica Técnica / Financeira | Regressão Linear (Campeão) | Random Forest | 
| :--- | :---: | :---: |
| **Coeficiente $R^2$ (Explicação)** | **94.40%** | 92.41% |
| **Erro Médio Absoluto (MAE)** | **R$ 38.582,21** | R$ 45.094,24 |
| **Erro Percentual Médio (MAPE)** | **6.19%** | 7.48% |

### 💡 Conclusão de Negócio
O modelo de **Regressão Linear** foi selecionado para o deploy devido à sua maior generalização e menor erro percentual médio (**6.19%**). Isso significa que, para um imóvel padrão de **R$ 600.000,00**, o modelo estima o valor de mercado com uma margem média de oscilação de apenas **R$ 38.582,21**.

---

## 🛠️ Tecnologias Utilizadas

* **Python** (Linguagem base)
* **Pandas** e **NumPy** (Manipulação e engenharia de dados)
* **Scikit-Learn** (Pré-processamento e Algoritmos de Machine Learning)
* **Matplotlib** e **Seaborn** (Visualização gráfica)

---

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git


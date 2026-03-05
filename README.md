# 📡 Telecom X - Previsão de Churn (Evasão de Clientes)

![Status do Projeto](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Linguagem](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Área-Machine%20Learning-orange)

## 📋 Sobre o Desafio
Este projeto foi desenvolvido como parte do desafio de modelagem preditiva para a empresa **Telecom X**. O objetivo principal é antecipar a evasão de clientes (Churn), permitindo que a empresa tome ações preventivas de retenção.

Como Analista de Machine Learning, minha missão foi construir um pipeline completo: desde o tratamento de dados brutos até a interpretação estratégica dos modelos de classificação.

## 🧰 Tecnologias e Ferramentas Utilizadas
- **Linguagem:** Python
- **Bibliotecas:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
- **Modelos Treinados:**
  - Dummy Classifier (Baseline)
  - K-Nearest Neighbors (KNN)
  - Árvore de Decisão
  - LinearSVC (Support Vector Classifier)

## 🛠️ Pipeline do Projeto

### 1. Pré-processamento e Limpeza
- Remoção de identificadores irrelevantes (`ID_Cliente`).
- Tratamento de valores nulos na variável alvo (`Churn`).
- **Encoding:** Transformação de variáveis binárias (Sim/Não) para (1/0) e aplicação de *One-Hot Encoding* para categorias múltiplas.
- **Escalonamento:** Aplicação de `StandardScaler` para normalizar as variáveis, garantindo que colunas com grandes magnitudes (ex: Valor Total) não enviesassem modelos baseados em distância (KNN e SVC).

### 2. Análise Exploratória e Correlação
Identificamos os principais "sensores" de evasão:
- **Tempo de Contrato:** Variável com maior impacto negativo (quanto mais meses de contrato, menor o Churn).
- **Fibra Óptica:** Clientes com esta tecnologia apresentam maior taxa de cancelamento.
- **Tipo de Contrato:** Contratos mensais são mais propensos à evasão que os anuais.

### 3. Modelagem e Avaliação
Os modelos foram avaliados com base em Acurácia, Precisão, Recall e F1-Score.

| Modelo | Acurácia (Teste) | F1-Score |
| :--- | :--- | :--- |
| **LinearSVC** | **80.06%** | **0.58** |
| Árvore de Decisão | 78.71% | 0.53 |
| KNN | 76.79% | 0.52 |

O **LinearSVC** foi selecionado como o melhor modelo devido à sua estabilidade e melhor equilíbrio entre capturar clientes em risco (Recall) e evitar alarmes falsos (Precisão).

## 🚀 Conclusões e Estratégia
O projeto resultou em recomendações estratégicas para a Telecom X:
1. **Foco no Onboarding:** Implementar ações de retenção nos primeiros 6 meses de contrato.
2. **Revisão da Fibra:** Investigar a estabilidade técnica e precificação do serviço de Fibra Óptica.
3. **Incentivo à Fidelidade:** Criar campanhas para migração de contratos mensais para anuais.

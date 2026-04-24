# Titanic Survival Prediction 🚢

Um projeto focado em análise exploratória de dados e machine learning, desenvolvido para composição de portfólio e aprimoramento prático de conceitos analíticos. Este repositório contém um script que executa uma pipeline ponta a ponta, desde a extração dos dados até a avaliação de um modelo de classificação baseado no clássico dataset do Titanic.

## 🎯 Objetivo do Projeto
O objetivo principal foi construir e avaliar um modelo preditivo capaz de classificar a probabilidade de sobrevivência dos passageiros. A estruturação do código segue as melhores práticas de processamento de dados, dividindo o problema em etapas claras de extração, transformação e modelagem.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Linguagem:** Python
* **Manipulação e Estruturação de Dados:** Pandas, NumPy
* **Visualização Analítica:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Logistic Regression)
* **Integração de Dados:** Kagglehub (Download via API)

## ⚙️ Arquitetura da Pipeline

O script `titanic_survival_prediction.py` está estruturado nas seguintes etapas:

1. **Extração (Data Loading):**
   * Download automatizado do dataset `yasserh/titanic-dataset` diretamente do Kaggle.
   * Estruturação inicial do DataFrame, definindo `PassengerId` como índice.

2. **Limpeza de Dados (Data Cleaning):**
   * Remoção de colunas com ruído ou que exigem processamento complexo de NLP nesta iteração inicial (`Cabin`, `Name`, `Ticket`).
   * Tratamento de valores ausentes (NaN), incluindo a imputação da média estatística na coluna `Age` e remoção residual de registros nulos.

3. **Engenharia de Features (Feature Engineering):**
   * Transformação de variáveis categóricas em numéricas (Encoding):
     * `Sex`: Mapeamento de male (0) e female (1).
     * `Embarked`: Mapeamento das portas S (0), C (1) e Q (2).

4. **Análise Exploratória de Dados (EDA):**
   * Geração de um *Heatmap* de correlação (com máscara triangular superior) para identificar as dependências entre as variáveis.
   * Criação de painéis de distribuição (KDE Histograms) gerados dinamicamente para visualizar o formato dos dados em todas as colunas numéricas.

5. **Modelagem e Avaliação (Modeling):**
   * Separação dos dados em conjuntos de Treino (80%) e Teste (20%), utilizando o parâmetro `stratify` para garantir que a proporção da variável alvo (`Survived`) seja preservada em ambas as amostras.
   * Treinamento e predição utilizando o modelo de **Regressão Logística**.
   * Cálculo final de métricas de performance do modelo estatístico (Acurácia, Precisão e Recall).

## 🚀 Como Executar o Projeto

Para rodar este script no seu ambiente local utilizando o Prompt de Comando (CMD), siga as instruções abaixo:

1. Clone o repositório para sua máquina:
   ```cmd
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   cd seu-repositorio

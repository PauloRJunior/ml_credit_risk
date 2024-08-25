# Credit Risk Classification

## Objetivo
O objetivo deste projeto é prever o risco de crédito de clientes com base em diversas características pessoais e financeiras. A classificação visa identificar se um cliente possui um alto risco de inadimplência em um empréstimo.

## Técnicas Utilizadas
O projeto utiliza várias técnicas e algoritmos para a construção de um modelo de classificação:

1. **Pré-processamento dos Dados:**
   - Imputação de valores ausentes usando `SimpleImputer`.
   - Escalonamento das variáveis numéricas com `MinMaxScaler`.
   - Codificação das variáveis categóricas com `OneHotEncoder`.

2. **Modelos Utilizados:**
   - Regressão Logística (`LogisticRegression`)
   - Árvore de Decisão (`DecisionTreeClassifier`)
   - Floresta Aleatória (`RandomForestClassifier`)

3. **Validação do Modelo:**
   - Utilização de validação cruzada estratificada com `StratifiedKFold` para garantir uma distribuição balanceada das classes durante o treinamento.
   - Avaliação dos modelos com métricas como Log-Loss, precisão, recall, curva ROC e matriz de confusão.

## Resultados Obtidos
Os resultados obtidos indicam um desempenho robusto para a classe sem risco (Classe 0), com uma área sob a curva ROC (AUC) de 0.91. Entretanto, a classe de risco (Classe 1) apresentou uma taxa de falsos negativos de 31%, sugerindo que há espaço para melhorar o recall desta classe.

### Métricas:
- **AUC Classe 0:** 0.91
- **AUC Classe 1:** 0.91
- **AUC Média Micro:** 0.95
- **AUC Média Macro:** 0.91
- **Log-Loss Médio:** Variável entre os modelos, com a Regressão Logística apresentando o melhor desempenho.

## Como Executar o Projeto

### 1. Clone o Repositório
```bash
git clone <link-do-repositorio>

pip install -r requirements.txt

jupyter notebook CreditRiskClassification.ipynb
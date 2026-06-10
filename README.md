# Análise de Preços de Casas com Machine Learning

Projeto desenvolvido para a disciplina **Análise de Dados Aplicada à Computação** do curso de **Sistemas de Informação - FAESA**.

---

## Integrantes

* Hellen Karla Costa Campos Moraes de Melo
* José Henrique Bessi Wolkers
* Kaio Soares Pacheco
* Yasmim Luiz dos Santos
  
---

## Sobre o Projeto

Este projeto tem como objetivo analisar um conjunto de dados de preços de casas nos Estados Unidos, utilizando análise de dados e Machine Learning.

A partir do dataset **House Prices - Advanced Regression Techniques**, o trabalho busca entender quais características das casas podem influenciar no preço de venda, além de aplicar modelos supervisionados e técnicas não supervisionadas para prever, classificar e agrupar imóveis com características semelhantes.

---

## Objetivo Geral

Explorar os dados de preços de casas, realizar o tratamento das variáveis e aplicar modelos de Machine Learning para prever preços, classificar imóveis em faixas de valor e agrupar casas com características semelhantes.

---

## Problema de Pesquisa

> Quais características das casas influenciam o preço de venda e como os dados podem ajudar a identificar padrões entre os imóveis?

---

## Metodologia

O desenvolvimento do projeto segue as seguintes etapas:

### 1. Coleta ou Carregamento dos Dados

- Importação do dataset
- Leitura dos arquivos utilizados
- Entendimento inicial das variáveis presentes na base

### 2. Tratamento dos Dados

- Verificação de valores ausentes
- Separação entre variáveis numéricas e categóricas
- Tratamento básico dos valores faltantes
- Codificação de variáveis categóricas
- Padronização dos dados para aplicação dos modelos

### 3. Análise Exploratória dos Dados

- Análise inicial do tamanho da base
- Verificação dos tipos de variáveis
- Análise estatística da variável `SalePrice`
- Visualização da distribuição dos preços
- Identificação de possíveis valores extremos
- Análise de correlações entre variáveis numéricas
- Criação de gráficos para melhor visualização dos dados

### 4. Feature Engineering

- Criação da variável `Idade_Casa`
- Criação da variável `Idade_Reforma`
- Criação da variável `Total_Banheiros`
- Criação da variável `Area_Total`
- Criação da variável `Preco_Alto` para classificação binária
- Seleção de variáveis relevantes para os modelos

### 5. Aplicação das Técnicas

- Regressão Linear Múltipla
- Classificação com KNN
- Clusterização com K-Means
- Redução de dimensionalidade com PCA
- Análise de associação com Apriori
- Análise de outliers com Local Outlier Factor

### 6. Interpretação dos Resultados

- Avaliação dos modelos criados
- Comparação entre as principais métricas
- Interpretação dos agrupamentos
- Análise dos possíveis outliers encontrados
- Discussão dos principais padrões observados

---

## Tecnologias Utilizadas

| Tecnologia | Finalidade |
|---|---|
| Python | Linguagem principal do projeto |
| Pandas | Manipulação e análise de dados |
| NumPy | Operações numéricas |
| Matplotlib | Criação de gráficos |
| Seaborn | Visualizações estatísticas |
| Scikit-learn | Modelagem e Machine Learning |
| Mlxtend | Aplicação do algoritmo Apriori |
| Jupyter Notebook | Desenvolvimento e documentação da análise |

---

## Estrutura do Projeto

```bash
House-Prices-Analise/
│
├── Trabalho_C3_House_Prices.ipynb
├── train.csv
├── test.csv
├── sample_submission.csv
└── README.md
````

---

## Dataset Utilizado

Dataset: **House Prices - Advanced Regression Techniques**

A base de dados contém informações sobre casas localizadas nos Estados Unidos, incluindo características físicas, estruturais e informações relacionadas à venda dos imóveis.

Principais informações presentes no dataset:

* Área do imóvel
* Número de quartos
* Número de banheiros
* Qualidade geral da casa
* Ano de construção
* Tamanho da garagem
* Bairro onde a casa está localizada
* Preço de venda da casa

A variável principal utilizada na análise foi `SalePrice`, que representa o preço de venda dos imóveis.

---

## Principais Análises Realizadas

Durante o desenvolvimento do projeto, foram realizadas análises para compreender melhor o comportamento dos preços das casas e a relação entre as variáveis.

Entre as principais análises, destacam-se:

* Análise da distribuição do preço de venda (`SalePrice`)
* Verificação de valores ausentes
* Identificação de variáveis numéricas e categóricas
* Análise de correlação entre as variáveis numéricas e o preço
* Visualização da relação entre `GrLivArea` e `SalePrice`
* Visualização da relação entre `OverallQual` e `SalePrice`
* Criação de novas variáveis para melhorar a análise
* Aplicação de modelos supervisionados para regressão e classificação
* Aplicação de técnicas não supervisionadas para agrupamento, associação e detecção de outliers

Na análise exploratória, foi observado que a variável `SalePrice` possui uma distribuição assimétrica, com a maior parte das casas concentrada em uma faixa de preço intermediária e alguns imóveis com valores muito mais altos.

As variáveis que mais se destacaram na relação com o preço foram:

* `OverallQual`: qualidade geral do imóvel
* `GrLivArea`: área útil acima do solo
* `GarageCars`: capacidade da garagem
* `TotalBsmtSF`: área total do porão
* `Total_Banheiros`: quantidade total de banheiros
* `Area_Total`: área total calculada no projeto

---

## Resultados Obtidos

### Regressão Linear Múltipla

A Regressão Linear Múltipla foi utilizada para prever o preço de venda das casas a partir de variáveis numéricas selecionadas.

O modelo apresentou os seguintes resultados:

| Métrica | Resultado aproximado |
| ------- | -------------------: |
| MAE     |               24.683 |
| RMSE    |               37.534 |
| R²      |                0,798 |

O valor de **R² de aproximadamente 0,798** indica que o modelo conseguiu explicar cerca de **79,8% da variação dos preços** das casas. Esse resultado foi considerado satisfatório para uma primeira modelagem com variáveis selecionadas.

O **MAE de aproximadamente 24,7 mil dólares** indica o erro médio das previsões. Já o **RMSE de aproximadamente 37,5 mil dólares** mostra que existem alguns erros maiores, principalmente em imóveis com preços mais altos ou fora do padrão.

---

### Classificação com KNN

Para a classificação, a variável `SalePrice` foi transformada em uma variável binária chamada `Preco_Alto`, separando as casas em preço alto e preço baixo com base na mediana.

O modelo KNN apresentou:

| Métrica  | Resultado aproximado |
| -------- | -------------------: |
| Acurácia |                91,8% |

A matriz de confusão mostrou que o modelo classificou corretamente a maior parte das casas das duas classes:

* 212 casas de preço baixo classificadas corretamente
* 190 casas de preço alto classificadas corretamente
* 21 casas de preço baixo classificadas como preço alto
* 15 casas de preço alto classificadas como preço baixo

Com isso, o modelo apresentou um bom desempenho para separar casas entre preço alto e preço baixo.

---

### Clusterização com K-Means

A clusterização com K-Means foi utilizada para agrupar casas com características semelhantes, sem utilizar diretamente a variável `SalePrice` como resposta.

Foram criados **3 clusters**, que representaram perfis diferentes de imóveis:

| Cluster   | Interpretação                                          |
| --------- | ------------------------------------------------------ |
| Cluster 0 | Casas de padrão intermediário                          |
| Cluster 1 | Casas de maior padrão, maior área e maior preço médio  |
| Cluster 2 | Casas mais simples, com menor área e menor preço médio |

O **score da silhueta foi de aproximadamente 0,282**, indicando uma separação moderada/fraca entre os grupos. Mesmo assim, os clusters ajudaram a identificar perfis diferentes de imóveis.

---

### Redução de Dimensionalidade com PCA

O PCA foi utilizado para visualizar os agrupamentos em duas dimensões.

Os dois primeiros componentes principais explicaram aproximadamente:

| Componente             | Variância explicada |
| ---------------------- | ------------------: |
| Componente Principal 1 |               65,9% |
| Componente Principal 2 |               10,8% |

Somando os dois componentes, a visualização preservou cerca de **76,7% das informações principais** das variáveis utilizadas na clusterização.

---

### Associação com Apriori

A análise de associação com Apriori foi utilizada para encontrar combinações frequentes entre características categóricas das casas.

Entre os padrões mais frequentes, apareceram variáveis relacionadas a:

* Condição de venda
* Qualidade da cozinha
* Estilo da casa
* Bairro
* Faixa de preço

As regras de associação ajudaram a identificar combinações comuns entre características dos imóveis, mas foram interpretadas como associação, e não como relação de causa direta com o preço.

---

### Análise de Outliers com Local Outlier Factor

O Local Outlier Factor foi utilizado para identificar registros com comportamento diferente da maioria dos dados.

O modelo identificou:

| Tipo de registro   | Quantidade |
| ------------------ | ---------: |
| Não outliers       |       1327 |
| Possíveis outliers |        133 |

Os outliers apareceram principalmente em imóveis com área muito alta e preço relativamente baixo, ou imóveis com preço muito elevado em comparação com casas de características semelhantes.

---

## Comparação Geral das Métricas

| Técnica                   | Tipo de problema   | Métrica principal | Resultado |
| ------------------------- | ------------------ | ----------------- | --------: |
| Regressão Linear Múltipla | Regressão          | R²                |     0,798 |
| KNN                       | Classificação      | Acurácia          |     91,8% |
| K-Means                   | Não supervisionado | Score da Silhueta |     0,282 |

A comparação foi feita considerando que cada técnica possui um objetivo diferente.

A Regressão Linear busca prever um valor numérico, a classificação com KNN busca separar as casas em categorias e o K-Means busca encontrar grupos de casas semelhantes.

Por isso, as métricas não foram comparadas diretamente como se medissem a mesma coisa, mas sim interpretadas dentro do objetivo de cada modelo.

---

## Conclusão

Com base nas análises realizadas, foi possível observar que o preço de venda das casas está relacionado principalmente a características como **qualidade geral do imóvel**, **área construída**, **tamanho da garagem**, **área do porão** e **quantidade total de banheiros**.

A **Regressão Linear Múltipla** apresentou um desempenho satisfatório para prever o preço das casas, com R² de aproximadamente **0,798**.

A **classificação com KNN** apresentou bom resultado para separar imóveis entre preço alto e preço baixo, alcançando aproximadamente **91,8% de acurácia**.

Na parte de **aprendizagem não supervisionada**, o **K-Means** permitiu agrupar os imóveis em três perfis principais: casas mais simples, casas intermediárias e casas de maior padrão. O **PCA** ajudou na visualização desses grupos em duas dimensões.

Além disso, o **Apriori** permitiu encontrar combinações frequentes entre características categóricas, enquanto o **Local Outlier Factor** identificou imóveis com comportamento fora do padrão.

De forma geral, o projeto cumpriu o objetivo de aplicar técnicas de análise de dados e Machine Learning para compreender melhor os fatores que influenciam o preço dos imóveis. Mesmo utilizando modelos simples, foi possível identificar padrões relevantes, prever preços, classificar imóveis, formar grupos e detectar registros fora do padrão.

---

## Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/House-Prices-Analise.git
```

### 2. Acesse a pasta do projeto

```bash
cd House-Prices-Analise
```

### 3. Instale as dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn mlxtend notebook
```

### 4. Execute o Jupyter Notebook

```bash
jupyter notebook
```

Depois, abra o arquivo:

```bash
Trabalho_C3_House_Prices.ipynb
```

---

## Disciplina

**Análise de Dados Aplicada à Computação**
Centro Universitário FAESA

---

## Licença

Projeto acadêmico desenvolvido exclusivamente para fins educacionais.

```
```

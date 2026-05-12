# Análise de Preços de Casas com Machine Learning

Projeto desenvolvido para a disciplina **Análise de Dados Aplicada à Computação** do curso de **Sistemas de Informação - FAESA**.

---

## Sobre o Projeto

Este projeto tem como objetivo analisar um conjunto de dados de preços de casas nos Estados Unidos, utilizando análise de dados e Machine Learning.

A partir do dataset **House Prices - Advanced Regression Techniques**, o trabalho busca entender quais características das casas podem influenciar no preço de venda, além de aplicar modelos supervisionados e técnicas não supervisionadas.

---

## Objetivo Geral

Explorar os dados de preços de casas, realizar o tratamento das variáveis e aplicar modelos de Machine Learning para prever, classificar e agrupar casas com características semelhantes.

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
- Análise da variável `SalePrice`
- Identificação de correlações entre variáveis numéricas
- Criação de gráficos para melhor visualização dos dados

### 4. Aplicação das Técnicas

- Regressão Linear
- Classificação com KNN
- Clusterização com K-Means
- Redução de dimensionalidade com PCA
- Análise de associação com Apriori
- Análise de outliers com Local Outlier Factor

### 5. Interpretação dos Resultados

- Avaliação dos modelos criados
- Comparação simples entre os resultados
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

---

## Principais Análises Realizadas



---

## Resultados Obtidos



---

## Status do Projeto



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

## Integrantes

* Hellen Karla Costa Campos Moraes de Melo
* José Henrique Bessi Wolkers
* Kaio Soares Pacheco
* Yasmim Luiz dos Santos

---

## Disciplina

**Análise de Dados Aplicada à Computação**
Centro Universitário FAESA

---

## Licença

Projeto acadêmico desenvolvido exclusivamente para fins educacionais.


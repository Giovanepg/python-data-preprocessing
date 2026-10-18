# 📊 Análise e Tratamento de Dados com Python

Este repositório reúne **cinco atividades práticas de Ciência de Dados**, desenvolvidas utilizando Python e suas bibliotecas para análise, limpeza e preparação de dados.

O objetivo das atividades é trabalhar com diferentes conjuntos de dados reais, identificando problemas de qualidade e aplicando técnicas para preparar os dados para análises posteriores.

As atividades foram desenvolvidas em **Jupyter Notebook**, utilizando principalmente Pandas, NumPy, Matplotlib, Seaborn e Scikit-learn.

---

## 📚 Índice

1. [Tecnologias utilizadas](#-tecnologias-utilizadas)
2. [Atividade 1 — Tratamento de Valores Ausentes](#-atividade-1--tratamento-de-valores-ausentes)
3. [Atividade 2 — Identificação de Duplicatas](#-atividade-2--identificação-de-duplicatas)
4. [Atividade 3 — Padronização e Escalonamento](#-atividade-3--padronização-e-escalonamento)
5. [Atividade 4 — Detecção de Outliers](#-atividade-4--detecção-de-outliers)
6. [Atividade 5 — Pipeline de Limpeza](#-atividade-5--pipeline-de-limpeza)
7. [Como executar](#-como-executar)
8. [Conclusão](#-conclusão)

---

## 🛠 Tecnologias utilizadas

- **Python:** linguagem de programação utilizada nas atividades.
- **Pandas:** manipulação e análise de DataFrames.
- **NumPy:** operações e cálculos numéricos.
- **Matplotlib:** criação de gráficos.
- **Seaborn:** visualização de dados estatísticos.
- **Missingno:** visualização de valores ausentes.
- **Scikit-learn:** técnicas de escalonamento.
- **Jupyter Notebook:** desenvolvimento e execução dos códigos.

---

## 📌 Atividade 1 — Tratamento de Valores Ausentes

**Dataset:** Melbourne Housing Snapshot

🔗 [Dataset no Kaggle](https://www.kaggle.com/datasets/dansbecker/melbourne-housing-snapshot)

### Objetivo

Identificar os valores ausentes em uma base de vendas de imóveis de Melbourne, na Austrália, e aplicar diferentes estratégias para o tratamento dessas informações.

### O que foi desenvolvido

- Carregamento do dataset utilizando Pandas.
- Análise das dimensões e tipos das colunas.
- Identificação da quantidade e porcentagem de valores ausentes.
- Visualização dos dados ausentes utilizando Missingno.
- Remoção de linhas com informações faltantes.
- Imputação utilizando mediana e moda.
- Comparação dos resultados das estratégias.

### Principais comandos

`read_csv()`, `isnull()`, `sum()`, `mean()`, `dropna()`, `fillna()`, `median()` e `mode()`.

### Aprendizado

A atividade permitiu compreender como identificar informações ausentes e avaliar duas formas de tratamento: remover registros incompletos ou preencher os valores faltantes com medidas estatísticas.

---

## 📌 Atividade 2 — Identificação de Duplicatas

**Dataset:** Customer Transaction Dataset (KPMG)

🔗 [Dataset no Kaggle](https://www.kaggle.com/datasets/archit9406/customer-transaction-dataset)

### Objetivo

Identificar registros duplicados em uma base de transações de clientes e avaliar como essas duplicatas podem influenciar os resultados de uma análise.

### O que foi desenvolvido

- Carregamento de uma planilha Excel.
- Conferência do cabeçalho e dos tipos das colunas.
- Identificação de duplicatas exatas.
- Verificação de duplicatas utilizando subconjuntos de colunas.
- Análise da unicidade dos identificadores de transações.
- Remoção de duplicatas exatas.
- Comparação da quantidade de registros e da soma dos preços antes e depois do tratamento.

### Principais comandos

`read_excel()`, `duplicated()`, `drop_duplicates()`, `is_unique()`, `copy()` e `sum()`.

### Aprendizado

A atividade mostrou a importância de verificar registros repetidos antes de calcular indicadores, além de demonstrar que registros semelhantes nem sempre representam a mesma transação.

---

## 📌 Atividade 3 — Padronização e Escalonamento

**Dataset:** Adult Census Income

🔗 [Dataset na UCI](https://archive.ics.uci.edu/dataset/2/adult)

### Objetivo

Encontrar inconsistências em dados demográficos e de renda, padronizar informações categóricas e aplicar diferentes técnicas de escalonamento às colunas numéricas.

### O que foi desenvolvido

- Carregamento de um arquivo sem cabeçalho.
- Identificação de categorias presentes nas colunas.
- Remoção de espaços extras nos textos.
- Substituição de marcadores de valores desconhecidos por `NaN`.
- Aplicação do escalonamento Min-Max.
- Aplicação da padronização Z-score.
- Aplicação do RobustScaler.
- Comparação de mínimos, máximos, médias e desvios-padrão.

### Principais comandos

`unique()`, `nunique()`, `str.strip()`, `replace()`, `select_dtypes()` e `fit_transform()`.

### Técnicas utilizadas

| Técnica | Descrição |
|---|---|
| Min-Max | Transforma os valores para uma escala entre 0 e 1 |
| Z-score | Padroniza os dados utilizando média e desvio-padrão |
| RobustScaler | Utiliza mediana e quartis, sendo menos sensível a valores extremos |

### Aprendizado

A atividade demonstrou a importância de corrigir inconsistências em dados categóricos e compreender como diferentes métodos de escalonamento modificam a escala dos valores numéricos.

---

## 📌 Atividade 4 — Detecção e Tratamento de Outliers

**Dataset:** Diamonds

🔗 [Dataset Diamonds — Seaborn](https://github.com/mwaskom/seaborn-data)

### Objetivo

Identificar valores extremos em uma base de preços e características físicas de diamantes, diferenciando possíveis erros de registro de valores extremos legítimos.

### O que foi desenvolvido

- Carregamento do dataset diretamente pelo Seaborn.
- Análise das estatísticas descritivas.
- Identificação de dimensões fisicamente inválidas.
- Detecção de outliers pelo método Z-score.
- Detecção de outliers pelo método IQR.
- Visualização por boxplots e gráficos de dispersão.
- Remoção de registros.
- Aplicação de capping.
- Transformação logarítmica dos preços.
- Comparação das estatísticas e distribuições após os tratamentos.

### Principais comandos

`describe()`, `mean()`, `std()`, `quantile()`, `boxplot()`, `scatterplot()`, `clip()` e `log1p()`.

### Técnicas utilizadas

| Técnica | Descrição |
|---|---|
| Z-score | Identifica valores distantes da média em desvios-padrão |
| IQR | Identifica valores fora dos limites calculados com quartis |
| Remoção | Exclui registros conforme critérios definidos |
| Capping | Substitui valores extremos pelos limites estabelecidos |
| Logaritmo | Reduz a diferença de escala entre valores baixos e altos |

### Aprendizado

A atividade permitiu compreender que nem todo outlier representa um erro. Valores muito elevados podem ser legítimos, enquanto dimensões físicas iguais a zero indicam problemas nos registros.

---

## 📌 Atividade 5 — Pipeline de Limpeza

**Dataset:** Dirty E-Commerce Data — SHEIN

🔗 [Dataset no Kaggle](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein)

### Objetivo

Integrar as técnicas estudadas anteriormente para realizar uma limpeza completa de dados de produtos de e-commerce, preparando as informações para análises de preços e descontos.

### Pergunta de negócio

**Quais categorias de produtos possuem os maiores preços médios e descontos médios?**

### O que foi desenvolvido

- Carregamento de dois arquivos CSV.
- Diagnóstico inicial da qualidade dos dados.
- Correção de tipos de dados.
- Tratamento de valores ausentes.
- Identificação e remoção de duplicatas.
- Padronização dos textos.
- Tratamento de valores extremos utilizando IQR e capping.
- Criação da coluna `faixa_preco`.
- Organização do processo de limpeza em funções reutilizáveis.
- Comparação de indicadores antes e depois da limpeza.
- Visualização dos resultados em gráficos.
- Exportação dos dados tratados para CSV.

### Funções utilizadas no pipeline

| Função | Finalidade |
|---|---|
| `corrigir_tipos()` | Converter preços e descontos em valores numéricos |
| `tratar_ausentes()` | Identificar e tratar informações faltantes |
| `tratar_duplicatas()` | Remover registros completamente iguais |
| `padronizar_textos()` | Remover espaços extras dos textos |
| `tratar_outliers()` | Identificar e limitar preços extremos |
| `criar_features()` | Criar uma nova coluna de classificação dos preços |

### Nova coluna criada

A coluna `faixa_preco` classifica os produtos em três grupos:

- **Baixo:** preços até 10.
- **Médio:** preços maiores que 10 e até 30.
- **Alto:** preços maiores que 30.

Os limites são utilizados como exemplo de classificação e podem ser ajustados conforme os dados.

### Aprendizado

A atividade reuniu os conhecimentos de limpeza e preparação de dados, demonstrando como organizar operações em funções reutilizáveis para facilitar o tratamento de diferentes arquivos de um mesmo dataset.

---


## 📖 Conclusão

As cinco atividades abordam etapas fundamentais da preparação de dados para análise e Ciência de Dados.

Durante o desenvolvimento, foram trabalhados problemas comuns em datasets reais, como valores ausentes, registros duplicados, informações inconsistentes, tipos incorretos e valores extremos.

Também foram aplicadas diferentes estratégias de tratamento, técnicas de escalonamento, visualizações e funções reutilizáveis.

O desenvolvimento dessas atividades contribuiu para a prática com Python e Pandas, além de proporcionar uma melhor compreensão da importância da qualidade dos dados antes de realizar análises estatísticas ou utilizar modelos de Machine Learning.

---

**Projeto acadêmico — Ciência de Dados com Python.**

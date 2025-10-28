

##  Projeto: Controle e Versionamento de Código no Notebook da Azure

###  Descrição

Este projeto faz parte do desafio **"Controle e Versionamento de Código no Notebook da Azure"** da plataforma **DIO (Digital Innovation One)**.
O objetivo foi explorar o ambiente do **Azure Databricks**, criar um **notebook em Pandas** e realizar operações de **análise e filtragem de dados com o Apache Spark**.

Durante a prática, foi realizado um filtro para selecionar apenas os produtos da categoria **"Mountain Bikes"** e visualizar as informações principais, como *ProductID*, *ProductName*, *Category* e *ListPrice*.

---

###  Objetivo do Projeto

* Criar e executar um **notebook Python** dentro do **Azure Databricks**;
* Praticar comandos básicos de análise com **Apache Spark**;
* Entender o processo de filtragem de dados com DataFrames;
* Versionar o projeto no **GitHub** para compor o portfólio técnico.

---

###  Tecnologias Utilizadas

* **Microsoft Azure**
* **Azure Databricks**
* **Apache Spark**
* **Python (pandas e pyspark)**
* **Git e GitHub**

---

###  Etapas Realizadas

1. Criação de um workspace no **Azure Databricks**;
2. Criação de um **notebook Python**;
3. Carregamento de um DataFrame com os dados de produtos;
4. Aplicação de filtro para a categoria `"Mountain Bikes"`;
5. Exibição dos resultados em formato de tabela;
6. Registro e versionamento no **GitHub**.

---

###  Código Utilizado

```Pandas
# IMPORTANDO ARQUIVO CSV EM PANDAS CONVERTE PARA SPARK PARA VISUALIZAÇÃO DE DADOS DEVIDO NAO ESTA EM SERVELEES "
import pandas as pd

df_pd = pd.read_csv("https://raw.githubusercontent.com/MicrosoftLearning/mslearn-databricks/main/data/products.csv")
df_spark = spark.createDataFrame(df_pd)
display(df_spark)

# Filtrando apenas produtos da categoria "Mountain Bikes"

df_mountain_bikes_spark = df_spark.filter(df_spark.Category == "Mountain Bikes")
display(df_mountain_bikes_spark)display(df_mountain_bikes)
```

---

### 📊 Resultado

A consulta retornou os produtos da categoria **Mountain Bikes**, exibindo informações como *ProductID*, *ProductName*, *Category* e *ListPrice*.

| ProductID | ProductName             | Category       | ListPrice |
| --------- | ----------------------- | -------------- | --------- |
| 771       | Mountain-100 Silver, 38 | Mountain Bikes | 3399.99   |
| 772       | Mountain-100 Silver, 42 | Mountain Bikes | 3399.99   |
| ...       | ...                     | ...            | ...       |

---

### 📸 Evidências do Projeto

📌 **1️⃣ Notebook criado e executado no Azure Databricks**

> Mostra o notebook com o DataFrame carregado e a execução do código Python.
> ![Notebook no Databricks](ANALISE_DADOS_SPARK.png)

📌 **2️⃣ Filtragem dos produtos da categoria “Mountain Bikes”**

> Exibe o resultado do filtro aplicado no DataFrame com os produtos e preços listados.
> ![Filtro por categoria Mountain Bikes](filtrando_por_categoria.png)

📌 **3️⃣ Resultado final da execução**

> Demonstração do output exibido após o uso do `display(df_mountain_bikes)` mostrando as linhas filtradas.
> ![Resultado da execução](a563de33-f3d6-404c-a584-06f314f5faf1.png)

---

### 💬 Insights e Aprendizados

* O **Databricks** permite integrar Python, Spark e análise de dados em um ambiente visual e colaborativo.
* É possível realizar análises de grande escala de forma simples e rápida.
* Reforcei o entendimento de **DataFrames distribuídos** e **filtragem de dados com Spark**.
* A experiência ajudou a consolidar conceitos de **engenharia e análise de dados em nuvem**.

---


---

Se quiser, posso gerar esse conteúdo direto em um arquivo `README.md` pra você baixar e só **arrastar pro GitHub** (já com as imagens referenciadas).
Deseja que eu gere o arquivo `.md` com esse conteúdo completo?

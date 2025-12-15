![Banner do Projeto](http://d1ih8jugeo2m5m.cloudfront.net/2025/03/tendencias-do-ecommerce.webp)

#Análise de Dados de E-commerce Brasileiro (Olist)

> **Nota:** Este é um projeto de estudos focado em Análise Exploratória de Dados (EDA), manipulação de dataframes com Pandas e visualização de dados com bibliotecas interativas.

## 📋 Visão Geral

Este projeto realiza uma análise detalhada sobre o conjunto de dados públicos de E-commerce brasileiro disponibilizado pela Olist. O objetivo principal foi exercitar habilidades técnicas em Ciência de Dados enquanto se extraem insights de negócio reais sobre o comportamento do varejo online no Brasil entre os anos de **2016 e 2018**.

O notebook percorre todo o ciclo de uma análise de dados: desde a ingestão automatizada e limpeza dos dados, passando pela fusão de múltiplas tabelas relacionais, até a criação de visualizações estratégicas.

## ❓ Perguntas de Negócio e Objetivos

O desenvolvimento deste estudo foi guiado por quatro perguntas chave, que foram respondidas através da análise dos dados:

1.  **Sazonalidade:** Qual época do ano apresenta o maior faturamento?
2.  **Geografia:** Qual é o estado Brasileiro que possui o maior volume de compras?
3.  **Mix de Produtos:** Qual é a categoria de produto mais vendida?
4.  **Tendências de Fim de Ano:** Quais são os 5 tipos de itens mais vendidos especificamente em Dezembro?

## 🛠️ Tecnologias e Bibliotecas

O projeto foi desenvolvido em **Python** utilizando o ambiente Google Colab. As principais ferramentas foram:

* **Manipulação de Dados:** `pandas`, `numpy` (Limpeza e agregação).
* **Visualização:** `plotly` (gráficos interativos), `seaborn`, `matplotlib` (análises estatísticas).
* **Fonte de Dados:** `kagglehub` (Integração direta com a API do Kaggle).
* **Sistema:** `os`, `shutil` (Gerenciamento de arquivos).

## 📂 Estrutura do Dataset

Os dados foram extraídos do [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). O projeto trabalhou com a fusão (`merge`) das seguintes tabelas:

* `olist_orders_dataset`: Dados principais do pedido (status, datas).
* `olist_order_items_dataset`: Detalhes dos itens (preço, frete).
* `olist_products_dataset`: Categorias e características dos produtos.
* `olist_customers_dataset`: Localização dos clientes (Estado/Cidade).

## 📊 Metodologia Aplicada

1.  **Coleta e Preparação:** Download automatizado dos dados via `kagglehub` e criação de um dataset unificado através de *Left Joins* entre as tabelas relacionais.
2.  **Feature Engineering:** Extração de atributos temporais (Mês, Ano, Trimestre) e criação de rótulos para melhor visualização em eixos de gráficos.
3.  **Análise Exploratória:**
    * Criação de gráficos de linha para séries temporais de faturamento.
    * Rankings de estados e categorias utilizando gráficos de barras.
    * Análise cruzada (Stacked Bar) para entender a preferência de produtos por região.

## 🚀 Principais Conclusões e Insights

A análise revelou padrões importantes sobre o mercado brasileiro:

* **Pico de Faturamento:** O e-commerce apresentou um crescimento acelerado, atingindo seu ápice histórico entre o final de 2017 e o início de 2018.
* **Hegemonia de SP:** O estado de **São Paulo** lidera o ranking de pedidos com uma margem esmagadora (mais de 41 mil pedidos), refletindo a concentração econômica e logística do Sudeste.
* **Liderança de Categoria:** A categoria **"Cama, Mesa e Banho"** foi a campeã absoluta de vendas no período geral.
* **Efeito Sazonal (Dezembro):** No mês de Dezembro, a categoria **"Esporte e Lazer"** ganha destaque significativo, subindo no ranking, provavelmente impulsionada pelo verão, férias escolares e presentes de Natal.

## ⚙️ Como Executar

1.  Certifique-se de ter uma conta no Google (para usar o Colab) ou um ambiente Jupyter local.
2.  Instale as dependências necessárias:
    ```bash
    pip install kagglehub pandas numpy matplotlib plotly seaborn
    ```
3.  Execute o notebook. O script está configurado para baixar os dados automaticamente.

---
**Autor:** Letycia Locha

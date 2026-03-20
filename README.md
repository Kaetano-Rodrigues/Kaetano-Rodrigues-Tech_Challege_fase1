# 📊 Projeto de Engenharia e Análise de Dados — E-commerce (Olist)

## 📌 Visão Geral

Este projeto tem como objetivo a construção de uma tabela analítica final (camada Gold) a partir de dados transacionais de um e-commerce, permitindo análises de negócio voltadas para:

* Performance de vendas
* Comportamento de clientes
* Eficiência logística
* Satisfação do cliente

A solução segue boas práticas de engenharia de dados e modelagem analítica, preparando os dados para consumo em ferramentas de BI como Power BI.

---

## 🧱 Arquitetura de Dados

O pipeline segue o conceito de camadas:

* **Bronze:** Dados brutos (ingestão)
* **Silver:** Dados tratados e normalizados
* **Gold:** Dados agregados e prontos para análise

A tabela final construída neste projeto está na camada **Gold**, com granularidade ao nível de item de pedido enriquecido com informações de cliente, produto e entrega.

---

## ⚙️ Tecnologias Utilizadas

* Python (Pandas)
* SQL (quando aplicável)
* Databricks (ambiente de processamento)
* Delta Lake
* Power BI (consumo analítico)

---

## 📂 Estrutura do Projeto

```
📁 projeto-olist/
│
├── 📓 Notebook 1 - Tratamento da Base.ipynb   # Notebook principal (pipeline e transformação)
├── 📓 Notebook 2 - Analises   # Notebook voltado as analises 
├── 📄 README.md                          # Documentação do projeto
```

---

## 🔄 Pipeline de Transformação

O Notebook 1 - Tratamento da Base realiza as seguintes etapas:

### 1. Carregamento dos Dados

Leitura das bases intermediárias (camada Silver), incluindo:

* Pedidos
* Itens de pedido
* Clientes
* Produtos
* Avaliações

---

### 2. Tratamento e Limpeza

* Conversão de tipos de dados (datas, valores numéricos)
* Tratamento de valores nulos
* Padronização de colunas

---

### 3. Enriquecimento dos Dados

* Junção entre múltiplas tabelas
* Criação de métricas como:

  * Receita por item
  * Tempo de entrega
  * Indicadores de status

---

### 4. Criação da Tabela Final (Gold)

Construção de uma tabela analítica contendo:

* `order_id`
* `customer_unique_id`
* `product_id`
* `seller_id`
* `price`
* `freight_value`
* `item_total`
* Datas do ciclo do pedido
* Localização do cliente
* Categoria do produto
* Score de avaliação

---

### 5. Persistência dos Dados

A tabela final é salva em formato **Delta**, permitindo:

* Versionamento
* Escalabilidade
* Integração com ferramentas analíticas

E tambem em formato CSV.
---

## 📊 Possibilidades de Análise

A tabela final permite diversas análises estratégicas:

### 💰 Receita e Crescimento

* Evolução mensal de pedidos e faturamento
* Ticket médio

### 🛍️ Performance de Produtos e Sellers

* Top produtos por receita
* Sellers mais eficientes

### 🚚 Logística

* Tempo de entrega real vs estimado
* Identificação de gargalos

### 👤 Comportamento do Cliente

* RFM (Recência, Frequência, Monetização)
* Retenção e recompra

### ⭐ Satisfação

* Distribuição de avaliações
* Relação entre entrega e satisfação

---

## 🚀 Como Executar

1. Clone o repositório:

```
git clone https://github.com/Kaetano-Rodrigues/Kaetano-Rodrigues-Tech_Challege_fase1
```

2. Abra o notebook:

```
Notebook 1 - Tratamento da Base.ipynb
```

3. Execute as células sequencialmente

> ⚠️ Observação: Ajuste os caminhos de leitura/escrita conforme seu ambiente (local ou Databricks)

---

## 📈 Próximos Passos

* Construção de dashboards no Power BI
* Implementação de métricas de churn
* Modelos preditivos (ex: previsão de entrega)
* Otimização de frete por região

---

## 👨‍💻 Autor

**Kaetano Rodrigues**
Engenheiro de Computação | Data Engineer | BI

* Python | SQL | Power BI | Azure | Databricks

---

## 📄 Licença

Este projeto é de uso educacional e para portfólio.

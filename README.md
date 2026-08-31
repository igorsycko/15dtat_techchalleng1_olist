# Tech Challenge — Fase 1 | Case E-commerce Olist

Relatório executivo para investidores e acionistas do setor de e-commerce, baseado no
Brazilian E-Commerce Public Dataset by Olist (\~100 mil pedidos, 2016-2018).

## Integrantes do Grupo

* Érica de Oliveira — RM 376644
* Igor S. U. Ramalho — RM 376886
* Luana L. Reis — RM 376811
* Rafaele T. Lima — RM 376318
* Thiago S. do Nascimento — RM 376102

## Pergunta Norteadora

> Como a eficiência logística da Olist afeta o crescimento e a sustentabilidade da
> receita, e onde estão as maiores oportunidades para acelerar esse crescimento sem
> comprometer a experiência do cliente?

## Trilhas Analíticas

* Trilha principal: Crescimento e Receita
* Trilha secundária: Logística e SLA

## Análises Realizadas

|Notebook|Conteúdo|
|-|-|
|`01\\\_compreensao\\\_dos\\\_dados.ipynb`|Ingestão dos 9 CSVs, volumetria, nulos, duplicidade, consistência de datas|
|`02\\\_preparacao\\\_dos\\\_dados.ipynb`|Tratamento de outliers/nulos e modelagem dimensional (`data/processado/`)|
|`03\\\_kpis\\\_principais.ipynb`|KPIs de Crescimento, Logística e Satisfação, e o KPI executivo combinado|
|`04\\\_analise\\\_crescimento\\\_receita.ipynb`|Evolução temporal, geografia, categorias, sellers e recompra|
|`05\\\_analise\\\_logistica\\\_sla.ipynb`|Lead time, SLA, outliers, atraso por estado, atraso x satisfação e impacto financeiro|

## Estrutura do Repositório

```
tech-challenge-olist/
├── data/
│   ├── base/            # CSVs originais do Kaggle (não versionados no Git)
│   └── processado/      # Tabela fato e dimensões geradas pelo notebook 02 (não versionadas no Git)
├── notebooks/
│   ├── 01\\\_compreensao\\\_dos\\\_dados.ipynb
│   ├── 02\\\_preparacao\\\_dos\\\_dados.ipynb
│   ├── 03\\\_kpis\\\_principais.ipynb
│   ├── 04\\\_analise\\\_crescimento\\\_receita.ipynb
│   └── 05\\\_analise\\\_logistica\\\_sla.ipynb
├── documentos/
│   ├── dicionario\\\_de\\\_dados.md
│   ├── modelo\\\_dimensional.svg
│   └── data\\\_quality\\\_summary.csv

├── relatorios/

│   ├── relatorio\_executivo\_OLIST.docx
│   └── Tech-Challenge-Olist-Analise-de-E-commerce.pdf

├── requerimentos.txt
└── README.md
```

## Stack

Python (pandas, matplotlib, seaborn) para análise e tratamento dos dados, e
Power BI ou Tableau para os dashboards executivos.

## Como Rodar

```bash
# 1. Clonar o repositório
git clone <url-do-repo>
cd tech-challenge-olist

# 2. Criar ambiente virtual e instalar dependências
python -m venv venv
source venv/bin/activate  # Windows: venv\\\\Scripts\\\\activate
pip install -r requerimentos.txt

# 3. Baixar o dataset do Kaggle e salvar os CSVs em data/base/
#    https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

# 4. Abrir os notebooks
jupyter notebook notebooks/
```

O notebook `05\\\_analise\\\_logistica\\\_sla.ipynb` foi desenvolvido e testado no
Google Colab e carrega os dados de `/content/` em vez de `data/processado/`.
Para rodar localmente, basta subir `fato\\\_pedidos.csv`, `dim\\\_clientes.csv` e
`olist\\\_order\\\_reviews\\\_dataset.csv` para `/content/` no próprio Colab, ou
ajustar os três caminhos de leitura no início do notebook.

## Metodologia

Projeto conduzido seguindo o framework CRISP-DM: Compreensão do Negócio,
Compreensão dos Dados, Preparação, Análise/Modelagem, Avaliação e Entrega.

## Escopo e Limitações

Este repositório cobre a etapa de dados do case (compreensão, tratamento e
modelagem dimensional, documentadas em `documentos/dicionario\\\_de\\\_dados.md`) e
as análises completas das duas trilhas escolhidas — Crescimento e Receita
(`notebooks/04\\\_analise\\\_crescimento\\\_receita.ipynb`) e Logística e SLA
(`notebooks/05\\\_analise\\\_logistica\\\_sla.ipynb`).


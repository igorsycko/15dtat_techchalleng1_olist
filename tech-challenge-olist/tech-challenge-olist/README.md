# Tech Challenge — Fase 1 | Case E-commerce Olist

Relatório executivo para investidores e acionistas do setor de e-commerce, baseado no
Brazilian E-Commerce Public Dataset by Olist (~100 mil pedidos, 2016-2018).

## Pergunta Norteadora

> Como a eficiência logística da Olist afeta o crescimento e a sustentabilidade da
> receita, e onde estão as maiores oportunidades para acelerar esse crescimento sem
> comprometer a experiência do cliente?

## Trilhas Analíticas

- Trilha principal: Crescimento e Receita
- Trilha secundária: Logística e SLA

## Frentes de Trabalho

| Frente | Foco |
|---|---|
| Dados e Governança | Ingestão, limpeza, modelagem dimensional, dicionário de dados |
| Análise — Crescimento e Receita | Evolução de receita, categorias, top sellers |
| Análise — Logística e SLA | Lead time, atrasos, mapa de calor regional |
| Storytelling e Relatório Executivo | Narrativa e redação do relatório |
| BI, Apresentação e Vídeo | Dashboards, slides e vídeo executivo |

## Estrutura do Repositório

```
tech-challenge-olist/
├── data/
│   ├── base/            # CSVs originais do Kaggle (não versionados no Git)
│   └── processado/      # Tabela fato e dimensões geradas pelo notebook 02 (não versionadas no Git)
├── notebooks/
│   ├── 01_compreensao_dos_dados.ipynb
│   └── 02_preparacao_dos_dados.ipynb
├── documentos/
│   ├── dicionario_de_dados.md
│   └── data_quality_summary.csv
├── requerimentos.txt
└── README.md
```

Outras pastas (relatório final, apresentação, scripts reutilizáveis) serão
criadas conforme o projeto avançar para os próximos sprints.

## Stack

Python (pandas, matplotlib) para análise e tratamento dos dados, e Power BI ou
Tableau para os dashboards executivos.

## Como Rodar

```bash
# 1. Clonar o repositório
git clone <url-do-repo>
cd tech-challenge-olist

# 2. Criar ambiente virtual e instalar dependências
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requerimentos.txt

# 3. Baixar o dataset do Kaggle e salvar os CSVs em data/base/
#    https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

# 4. Abrir o notebook
jupyter notebook notebooks/
```

## Metodologia

Projeto conduzido seguindo o framework CRISP-DM: Compreensão do Negócio,
Compreensão dos Dados, Preparação, Análise/Modelagem, Avaliação e Entrega.

## Entregáveis

- [ ] Relatório executivo
- [ ] Apresentação executiva — link a incluir
- [ ] Vídeo executivo (até 5 minutos) — link a incluir

## Cronograma

Ver roteiro completo do projeto (20 dias, 4 sprints) no documento compartilhado do grupo.

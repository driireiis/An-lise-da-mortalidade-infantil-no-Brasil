# Análise OLAP da Mortalidade Infantil - DATASUS

Este repositório contém um projeto de análise OLAP (Processamento Analítico Online) aplicado aos dados de **mortalidade infantil no Brasil**. Utilizando dados do **DATASUS - SIM (Sistema de Informações sobre Mortalidade)**, o projeto visa gerar insights a partir da exploração visual e estatística das principais dimensões envolvidas, como sexo e localidade dos óbitos.

---

## Tecnologias e Bibliotecas Utilizadas

O projeto foi desenvolvido em **Python 3** com uso das seguintes bibliotecas:

### Bibliotecas de manipulação de dados:
- `pandas`
- `numpy`
- `sqlite3` (para conexão com banco de dados SQLite)

### Visualização de dados:
- `matplotlib.pyplot`
- `seaborn`
- `plotly.express`
- `plotly.graph_objects`
- `plotly.subplots.make_subplots`

### Outras:
- `os` (para manipulação de diretórios e arquivos)

---

##  Estrutura do Projeto

```
├── obitos_infantis_2023.db             # Banco de dados SQLite com os dados de mortalidade
├── consultas_olap.py                   # Script com as consultas e geração de gráficos
├── graficos_olap/                      # Pasta gerada automaticamente para armazenar os gráficos
├── video_apresentacao.mp4              # Vídeo de 1 minuto apresentando o projeto
└── README.md                           # Documentação do repositório (este arquivo)
```

---

##  Funcionalidades Implementadas

- **Conexão ao banco SQLite** com verificação da existência das tabelas.
- **Extração e análise** dos dados a partir das tabelas:
  - `obitos_masc_fem`: óbitos por sexo
  - `obitos_capitais`: óbitos por capital brasileira
- **Geração de gráficos OLAP**, incluindo:
  - Comparações por sexo
  - Comparações regionais
  - Gráficos interativos em HTML usando Plotly
- **Criação automática da pasta `graficos_olap/`** para salvar os arquivos exportados

---

##  Exemplos de Gráficos Gerados

- Gráficos de barras com `matplotlib` e `seaborn`
- Visualizações interativas com `plotly`
- Dashboards HTML organizados com `plotly.subplots`

Os arquivos gerados são salvos em `graficos_olap/` e podem ser utilizados para fins de apresentação e análise exploratória.

---

##  Vídeo Demonstrativo

Está incluído no repositório um vídeo de **1 minuto** contendo:

- Apresentação dos objetivos do projeto
- Execução do script e geração dos gráficos
- Interpretação dos resultados

---

##  Integrantes do Grupo

- Adriana Gomes dos Reis  
- Gabriel Aleixo  
- Danilo Menegaldo

---

##  Observações

- O projeto pode ser expandido com novas dimensões analíticas, como causas de morte, faixa etária e comparações temporais.
- A estrutura atual foi pensada para fácil manutenção, reaproveitamento e visualização dos dados.
- O uso de SQLite permite portabilidade e baixo custo de execução local.

---

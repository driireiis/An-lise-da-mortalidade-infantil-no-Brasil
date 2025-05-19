# Análise OLAP da Mortalidade Infantil - DATASUS

Este repositório contém um projeto de análise OLAP (Processamento Analítico Online) aplicado aos dados de mortalidade infantil no Brasil, utilizando dados do DATASUS - SIM (Sistema de Informações sobre Mortalidade). O projeto busca gerar insights a partir da exploração visual e estatística das principais dimensões, como sexo, localidade e outras variáveis relacionadas aos óbitos.

---

## Tecnologias e Bibliotecas Utilizadas

O projeto foi desenvolvido em Python 3 e utiliza as seguintes bibliotecas:

### Manipulação e análise de dados:
- pandas  
- numpy  
- sqlalchemy (para conexão com bancos de dados)  
- Pysus (para acesso aos dados do DATASUS)  

### Visualização de dados:
- matplotlib.pyplot  
- seaborn  
- plotly.express  
- plotly.graph_objects  
- plotly.subplots.make_subplots  
- ipywidgets (para interatividade em notebooks)  

### Dashboard web interativo:
- dash  
- dash_core_components (dcc)  
- dash_html_components (html)  
- dash_table  
- dash.dependencies  

### Outros:
- warnings (para gerenciar alertas e avisos)  

---

## Estrutura do Projeto

├── obitos_infantis_2023.db # Banco de dados SQLite com dados de mortalidade
├── consultas_olap.py # Script com consultas SQL e geração de gráficos e dashboards
├── dash_app.py # Aplicação Dash para visualização interativa dos dados
├── graficos_olap/ # Pasta gerada automaticamente para armazenar gráficos
├── video_apresentacao.mp4 # Vídeo de 1 minuto apresentando o projeto
└── README.md # Este arquivo

yaml
Copiar
Editar

---

## Funcionalidades Implementadas

- Conexão com banco SQLite usando SQLAlchemy, com verificação da existência das tabelas.  
- Extração e análise dos dados nas tabelas principais, como:  
  - `obitos_masc_fem`: óbitos por sexo  
  - `obitos_capitais`: óbitos por capital brasileira  
- Análises OLAP com filtros e agregações para explorar as dimensões:  
  - Sexo  
  - Região / localidade  
  - Faixa etária (quando disponível)  
- Geração de gráficos estáticos e interativos para análise exploratória, usando Matplotlib, Seaborn e Plotly.  
- Construção de dashboards web interativos com Dash, incluindo filtros dinâmicos para o usuário explorar os dados.  
- Criação automática da pasta `graficos_olap/` para salvar os gráficos exportados (em PNG ou HTML).  
- Tratamento de dados e limpeza utilizando pandas e numpy.  
- Uso da biblioteca Pysus para facilitar o acesso aos dados do DATASUS.  

---

## Exemplos de Visualizações

- Gráficos de barras e linhas para comparação de mortalidade por sexo e localidade.  
- Mapas interativos e gráficos em dashboard com filtros dinâmicos.  
- Dashboards HTML interativos utilizando `plotly.subplots` e componentes Dash.  
- Visualizações que permitem o cruzamento de variáveis para análises multidimensionais.  

---

## Vídeo Demonstrativo

O repositório contém um vídeo de 1 minuto que apresenta:  
- Objetivos do projeto  
- Demonstração da execução dos scripts e geração dos gráficos  
- Interpretação e insights gerados a partir dos dados  

---

## Como Executar

### Configurar o ambiente

Instale as bibliotecas necessárias:

```bash
pip install pandas numpy sqlalchemy matplotlib seaborn plotly dash ipywidgets pysus
Banco de Dados
O arquivo obitos_infantis_2023.db deve estar na raiz do projeto. Caso queira, pode usar o script para recriar o banco com os dados do DATASUS.

Rodar as consultas e gerar gráficos
Execute:

bash
Copiar
Editar
python consultas_olap.py
Os gráficos serão salvos na pasta graficos_olap/.

Executar dashboard interativo (opcional)
Para rodar a aplicação Dash:

bash
Copiar
Editar
python dash_app.py
Acesse no navegador o endereço informado no terminal (geralmente http://127.0.0.1:8050).

Possíveis Expansões
Inclusão de outras dimensões, como causas de morte e faixa etária detalhada.
```

Análises temporais e comparações históricas.

Integração com outras fontes de dados do DATASUS para enriquecer a análise.

Automatização da atualização dos dados.

Melhoria da interface do dashboard com novos filtros e visualizações.

Integrantes do Grupo
Adriana Gomes dos Reis

Gabriel Aleixo

Danilo Menegaldo

Observações Finais
A estrutura do projeto prioriza facilidade de manutenção, reutilização do código e visualização clara dos dados.

O uso de SQLite e SQLAlchemy garante portabilidade e flexibilidade para manipulação dos dados.

As bibliotecas Dash e Plotly proporcionam visualizações interativas acessíveis mesmo para usuários não técnicos.

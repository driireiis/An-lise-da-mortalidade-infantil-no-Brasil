123

# Analise-da-mortalidade-infantil-no-Brasil

#  Análise da Mortalidade Infantil no Brasil

## Autores
Danilo Menelgado, Adriana Gomes dos Reis e Gabriel Aleixo

## Objetivo
Estudo baseado em dados públicos para entender os fatores da mortalidade infantil no Brasil, com suporte à tomada de decisão.

## Fontes dos Dados
- DATASUS: https://datasus.saude.gov.br
- IBGE: https://www.ibge.gov.br
- OMS: https://www.who.int

## Tecnologias
- Python (pandas, SQLAlchemy)
- SQLite (simples e leve)
- Apache Airflow (para orquestração e agendamento de tarefas)
- Git + GitHub (versionamento)

## ETL
- `extract.py`: Leitura do CSV original
- `transform.py`: Padronização e tratamento
- `load.py`: Carga em banco SQLite
- `run_etl.py`: Executa todo o pipeline

## OLAP
- Roll-up, Drill-down, Slice, Dice com exportação para CSV
- Consultas em `olap/queries.py`

## Executar Local
```bash
pip install -r requirements.txt
python etl/run_etl.py
python olap/queries.py

# End-to-End Movie Data Indexing Pipeline

Um pipeline completo de ETL que extrai dados de filmes, faz transformações e os armazena em um índice do Elasticsearch, permitindo consultas eficientes e análises sobre o universo cinematográfico.

## Visão Geral

Este repositório implementa uma solução ‘end-to-end’ (fim-a-fim) para:
- Extrair dados de filmes de fontes como CSV/JSON ou APIs públicas.  
- Realizar limpeza, normalização e enriquecimento dos dados.  
- Carregar os dados transformados em um índice no Elasticsearch para busca e análise.  
- Permitir exploração interativa (por exemplo via Jupyter Notebook) ou execução automatizada.

O objetivo é demonstrar como montar um pipeline de dados para o domínio de filmes — ideal para aprendizado, prototipagem ou base para projetos maiores.

## Arquitetura

O processo principal segue três etapas típicas de ETL:

### Etapas
1. **Extração**: leitura de arquivos (ex: `data/…`), coleta de dados brutos de filmes.  
2. **Transformação**: limpeza de campos, tratamento de valores faltantes, formatação, enriquecimento (ex: adicionar categorias, metadados).  
3. **Carga**: submissão dos dados no índice do Elasticsearch, garantindo que o esquema esteja definido e que os documentos estejam acessíveis para consulta.

## Conteúdo do Repositório

- `data/` – Contém os arquivos brutos ou intermediários de dados de filmes.  
- `spark-jars/` – (Se aplicável) bibliotecas jar necessárias para execução em Apache Spark.  
- `movie_indexing_pipeline.ipynb` – Notebook Jupyter que guia a execução, desde a leitura de dados até a ingestão no Elasticsearch.  
- `Pipeline_Movie_Indexing.png` – Diagrama visual da arquitetura do pipeline.

## Pré-requisitos

Antes de executar o pipeline, garanta que:

- Você tenha o Elasticsearch instalado e em execução (versão compatível).  
- Tenha Python 3.x instalado com dependências: `elasticsearch` e `pyspark`
- (Opcional) Se usar Apache Spark, tenha Spark configurado corretamente.  
- Os dados de filmes estejam disponíveis no local esperado ou as credenciais/configurações da API estejam definidas.

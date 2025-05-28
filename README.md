# 🛠️ Projeto de Pipeline de Dados com AWS
Este projeto simula um cenário real de migração de dados de um banco MySQL on-premise para a nuvem AWS, utilizando ferramentas gratuitas e serviços gerenciados da AWS. O objetivo foi construir um pipeline de dados moderno, seguindo boas práticas de engenharia de dados, como ETL em camadas (bronze, silver, gold), orquestração de processos e controle de acesso.

####  🌐 Contexto
A simulação parte de um banco MySQL rodando em uma instância Amazon EC2 (representando o ambiente on-premise). A partir disso, os dados são migrados e processados com ferramentas da AWS que garantem automação, segurança e organização em camadas, resultando em um pipeline robusto e escalável.

#### 🧰 Tecnologias e Serviços Utilizados
- **Amazon EC2**: para simular o ambiente on-premise com MySQL instalado.

- **AWS DMS (Database Migration Service)**: replicação contínua dos dados do MySQL para o Amazon S3.

- **Amazon S3**: armazenamento dos dados organizados por estágio (bronze, silver, gold).

- **AWS Glue**: catalogação de dados no Glue Data Catalog.

- **AWS Step Functions**: orquestração do pipeline, com controle de fluxo, falhas e monitoramento.

- **AWS CloudWatch**: monitoramento dos processos e geração de logs.

- **AWS IAM**: controle de acesso e segurança entre os serviços.

#### ⚙️ Arquitetura da Solução
O pipeline foi desenhado em camadas, com uma sequência bem definida:

- **Bronze**: ingestão dos dados crus via DMS no S3.

- **Silver**: pré-processamento e transformação intermediária (fora do Glue, com scripts Python).

- **Gold**: dados prontos para análise e consumo.

A orquestração foi feita com Step Functions, coordenando a ordem das tarefas e integrando serviços como S3, Glue e CloudWatch para garantir automação e confiabilidade.

### 🎯 Objetivos do Projeto
- Aplicar na prática conceitos de engenharia e arquitetura de dados na nuvem.

- Construir uma solução serverless e de baixo custo.

- Explorar a integração entre múltiplos serviços AWS com foco educacional.

- Demonstrar o uso de Step Functions para orquestrar workflows de dados.

### ⚠️ Importante
Este projeto tem fins educacionais e foi construído com foco em boas práticas, mas não é indicado para uso em produção sem adaptações e melhorias voltadas a performance, escalabilidade e governança.

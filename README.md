---

# Desafio Técnico – Engenharia de Dados 🍻

Este repositório contém a solução para o desafio técnico de Engenharia de Dados, com foco na ingestão, transformação e análise de dados sobre cervejarias utilizando a API [Open Brewery DB](https://api.openbrewerydb.org/breweries).

## 📌 Objetivo

Construir um pipeline de dados utilizando Python, orquestrado com uma ferramenta à sua escolha, seguindo a **arquitetura de data lake em camadas (medalhão)**:

- **Camada Bronze:** dados brutos da API.
- **Camada Prata:** dados transformados em formato colunar e particionados por localização.
- **Camada Ouro:** visão analítica com agregações por tipo e localização de cervejarias.

---

## 🔧 Stack Utilizada

- **Linguagem:** Python
- **Orquestração:** [Airflow / Luigi / Mage / etc.] <!-- Edite conforme sua escolha -->
- **Processamento:** [PySpark / Pandas / etc.] <!-- Edite conforme sua escolha -->
- **Armazenamento:** Arquivos em formato Parquet / Delta Lake
- **Containerização:** Docker / Kubernetes (opcional, mas recomendável)

---

## 🚀 Pipeline de Dados

1. **Ingestão (Camada Bronze):**
   - Dados são consumidos da API pública Open Brewery DB.
   - Persistência dos dados brutos no data lake.

2. **Transformação (Camada Prata):**
   - Conversão dos dados para formato colunar (Parquet ou Delta).
   - Particionamento por localização (estado ou cidade).
   - Aplicação de limpezas e validações.

3. **Agregação (Camada Ouro):**
   - Criação de uma visão analítica com o número de cervejarias por tipo e localização.

---

## ⚠️ Monitoramento e Alertas

O pipeline inclui estratégias para:
- Tentativas automáticas em caso de falhas.
- Validação de qualidade dos dados.
- Logs estruturados.
- Alertas (e-mail, Slack, etc.) em caso de falhas ou dados inconsistentes.

---

## 🧪 Testes

Inclui casos de teste para as principais funções de transformação e ingestão de dados utilizando `pytest`.

---

## 🐳 Containerização (opcional)

A solução pode ser executada em ambiente containerizado via Docker:

```bash
docker-compose up --build
```

---

## ☁️ Serviços em Nuvem (opcional)

Caso deseje utilizar serviços em nuvem (S3, GCP, Azure Data Lake etc.), certifique-se de:
- Configurar as credenciais localmente (não envie para o GitHub).
- Instruções detalhadas estarão disponíveis no diretório `docs/`.

---

## 📂 Estrutura do Repositório

```
.
├── dags/                   # Pipelines do Airflow (ou scripts do orquestrador)
├── src/                    # Código-fonte e transformações
├── tests/                  # Casos de teste
├── data/                   # Camadas do data lake (bronze, prata, ouro)
├── docker/                 # Dockerfile e configs (se aplicável)
├── README.md
└── requirements.txt
```

---

## ✅ Critérios Avaliados

- Qualidade do código
- Clareza na arquitetura
- Eficiência do pipeline
- Documentação
- Tratamento de erros
- Monitoramento

---

## 📅 Prazo

O desafio deve ser entregue em até **1 semana** a partir da data de recebimento.

---

## 💬 Contato

Dúvidas ou sugestões? Fique à vontade para abrir uma issue ou entrar em contato.

---
FC Barcelona 2025/26 — Business Intelligence Dashboard

# Dashboard
<img width="679" height="379" alt="Captura de tela 2026-10-31 175611" src="https://github.com/user-attachments/assets/be80ed9b-f16b-4efd-baf2-efa24e8d3c56" />
<img width="676" height="379" alt="Captura de tela 2026-10-31 175624" src="https://github.com/user-attachments/assets/176ff597-50ac-411f-bad6-88311db06f12" />

# Sobre o projeto

Este projeto consiste na construção de uma solução completa de Business Intelligence para análise da temporada 2025/26 do FC Barcelona.

O projeto contempla desde a coleta dos dados até a estruturação em banco de dados relacional e a construção de visualizações interativas. Todo o fluxo foi desenvolvido simulando um cenário real de análise de dados.

---

# Objetivos

- Praticar PostgreSQL

- Estruturação de Banco de Dados

- Consultas SQL

- Power BI

- Criação de medidas DAX (TOPN, MAXX, CALCULATE e CONCATENATEX)

- Storytelling com dados

- Visualização e interpretação de indicadores esportivos

# Pipeline do Projeto

              FBref
                  │
                  ▼
         Coleta dos dados
                  │
                  ▼
          PostgreSQL Database
                  │
     ┌────────────┴────────────┐
     ▼                         ▼
Tabela matches               Tabela players
     │                         │
     └────────────┬────────────┘
                  ▼
          Modelagem Power BI
                  │
                  ▼
          Dashboard Final


(Nota: A extração foi realizada diretamente para o banco de dados).

---
# Modelagem do Banco de Dados

O banco de dados foi estruturado no PostgreSQL, focando na organização das informações das partidas e dos jogadores.

# Tabelas

matches: Dados gerais de cada partida (data, adversário, gols, posse de bola, etc.).

players: Estatísticas individuais de cada jogador (minutos, gols, assistências, cartões, etc.).

---
# Modelo Relacional

PostgreSQL & SQL

Toda a estrutura de armazenamento foi construída no PostgreSQL. Foram desenvolvidas consultas e rotinas para:

Criação das tabelas

Carga dos dados extraídos do FBref

Consultas analíticas e tratamento dos dados

Integração com o Power BI

---
# Indicadores

Os dashboards apresentam indicadores chave para análise da temporada:

Visão Geral da Temporada:
✅ Total de Jogos (57)
✅ Gols Marcados (144) e Média de Posse de Bola (68%)
✅ Vitórias (44), Empates e Derrotas
✅ Aproveitamento em casa e fora
✅ Evolução dos jogos ao longo dos meses

Análise de Jogadores:
✅ Top Artilheiros e Assistentes (Lamine Yamal liderando)
✅ Minutos jogados e Quantidade de partidas
✅ Participações em gols e Cartões
✅ Distribuição do elenco por posição
✅ Eficiência ofensiva por 90 minutos (Raphinha em destaque)

---
# Tecnologias

- PostgreSQL

- SQL

- Power BI

- DAX

---
# Fonte dos dados

Todos os dados estatísticos foram obtidos através do FBref:
https://fbref.com/

---
# Principais aprendizados

Durante o desenvolvimento deste projeto foram consolidados conhecimentos em:

- Estruturação de Bancos de Dados Relacionais

- Consultas avançadas em SQL

- Tratamento de dados (ex: correção da formatação da posse de bola)

- Criação de medidas DAX dinâmicas e cálculos complexos

- Data Visualization e Design de Dashboards

- Integração de ponta a ponta (Banco de Dados -> Ferramenta de BI)

---
# Autor

## Pedro Comas

LinkedIn: https://www.linkedin.com/in/pedrocomas/

GitHub: https://github.com/pedrocomas

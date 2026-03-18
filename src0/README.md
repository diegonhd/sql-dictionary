# Fundamentos de SQL - Módulo src0

Este diretório contém scripts de exemplo que cobrem os comandos fundamentais de SQL para consulta e manipulação de dados, utilizando o banco de dados `longlist.db`.

## 📂 Estrutura de Arquivos

Os arquivos estão numerados para seguir uma ordem lógica de aprendizado:

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `0-SELECT.sql` | **SELECT** | Seleção de colunas e consultas básicas. |
| `1-LIMIT.sql` | **LIMIT** | Restrição do número de linhas retornadas. |
| `2-WHERE.sql` | **WHERE** | Filtragem de dados com base em condições. |
| `3-NULL.sql` | **NULL** | Como lidar com valores ausentes ou nulos (`IS NULL`). |
| `4-LIKE.sql` | **LIKE** | Busca de padrões em strings usando curingas (`%`, `_`). |
| `5-compound.sql` | **Operadores Compostos** | Uso de `AND`, `OR` e `NOT` para filtros complexos. |
| `6-range.sql` | **Ranges** | Consultas de intervalo usando `BETWEEN` e `IN`. |
| `7-dates.sql` | **Datas** | Manipulação e filtragem de campos de data e hora. |
| `8-ORDER BY.sql` | **ORDER BY** | Ordenação de resultados (Ascendente e Descendente). |
| `9-aggregate.sql`| **Funções de Agregação** | Cálculos como `COUNT`, `SUM`, `AVG`, `MIN` e `MAX`. |

## 🛠️ Como Utilizar

Para executar qualquer um dos scripts acima no terminal (utilizando SQLite), use o comando:

```bash
sqlite3 longlist.db < nome_do_arquivo.sql
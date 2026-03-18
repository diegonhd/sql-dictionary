# Relacionamentos e Agrupamentos - Módulo src1

Este diretório contém scripts que abordam o próximo nível do SQL: como trabalhar com múltiplas tabelas, realizar agrupamentos complexos e operações de conjunto.

## 📂 Estrutura de Arquivos

Os arquivos aqui exploram a relação entre dados e a consolidação de informações:

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `groups.sql` | **GROUP BY / HAVING** | Agrupamento de registros e filtragem de resultados agregados. |
| `joins.sql` | **JOINS** | Junção de tabelas (Inner, Left, Right) usando chaves estrangeiras. |
| `nested.sql` | **Subqueries** | Consultas aninhadas (uma query dentro de outra) para filtros dinâmicos. |
| `sets.sql` | **Sets** | Operações de conjuntos: `UNION`, `INTERSECT` e `EXCEPT`. |

## 💾 Bancos de Dados Utilizados

Nesta seção, você alterna entre dois bancos para diferentes contextos:
* `longlist.db`: Geralmente usado para subqueries e conjuntos.
* `sea_lions.db`: Focado em exemplos de contagem e agrupamentos.

## 🛠️ Como Utilizar

Para executar os scripts, escolha o banco de dados apropriado e rode no terminal:

```bash
# Exemplo para testar junções
sqlite3 sea_lions.db < joins.sql

# Exemplo para testar operações de conjunto
sqlite3 longlist.db < sets.sql
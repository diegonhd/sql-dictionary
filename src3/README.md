# Manipulação e Automação de Dados - Módulo src3

Este diretório aborda o ciclo completo de manipulação de dados (CRUD), técnicas de importação de arquivos externos, limpeza de dados e automação de processos via gatilhos (triggers).

## 📂 Estrutura de Arquivos

Abaixo estão os scripts organizados por tipo de operação e subpastas:

| Arquivo / Pasta | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `insert/insert0.sql` | **INSERT / Violations** | Demonstra inserções individuais e testes de violação de restrições (`UNIQUE` e `NOT NULL`). |
| `insert/insert1.sql` | **Bulk Insert** | Inserção de múltiplos registros em um único comando `VALUES`. |
| `update/update0.sql` | **Subqueries** | Atualização de registros utilizando subconsultas para correlacionar IDs. |
| `update/update1.sql` | **Data Cleaning** | Limpeza de dados usando `trim()`, `upper()` e operadores `LIKE`. |
| `update/update2.sql` | **Cleanup** | Remoção de entradas inválidas identificadas durante a limpeza. |
| `delete/delete0.sql` | **DELETE Básico** | Remoção física de registros baseada em filtros específicos. |
| `delete/delete1.sql` | **FK Constraints** | Demonstração de erros de integridade ao deletar registros com chaves estrangeiras ativas. |
| `delete/delete2.sql` | **CASCADE** | Uso de `ON DELETE CASCADE` para remoção automática de registros dependentes. |
| `delete/soft/` | **Soft Delete** | Estratégia de exclusão lógica utilizando uma coluna de status e o comando `UPDATE`. |
| `import/` | **.import** | Técnicas de importação de CSV, incluindo o uso de tabelas temporárias para gerenciar chaves primárias. |
| `triggers/triggers.sql`| **Triggers** | Automação de logs (auditoria) para operações de compra e venda usando gatilhos `BEFORE` e `AFTER`. |

## 💾 Bancos de Dados Utilizados

* **`mfa.db`**: Utilizado para os exemplos de museu (inserção, atualização, deleção e triggers).
* **`votes.db`**: Focado na limpeza de dados de votações populares.

## 🛠️ Como Utilizar

Para testar as automações de gatilhos:
```bash
sqlite3 mfa.db < triggers/triggers.sql
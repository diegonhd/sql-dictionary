# Design e Evolução de Bancos de Dados - Módulo src2

Este diretório foca na criação progressiva de um esquema robusto para o banco de dados `mbta.db` e no uso de comandos para modificar estruturas de dados existentes sem a necessidade de reconstruir o banco do zero.

## 📂 Subpasta: `alter/`

Scripts focados no comando `ALTER TABLE` para manutenção e correção de tabelas.

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `alter0.sql` | **DROP TABLE** | Demonstra como remover permanentemente a tabela `riders`. |
| `alter1.sql` | **RENAME TO** | Renomeia a tabela `visits` para `swipes`. |
| `alter2.sql` | **ADD COLUMN** | Adiciona uma nova coluna (`ttpe`) a uma tabela existente. |
| `alter3.sql` | **RENAME COLUMN** | Corrige um erro de digitação renomeando a coluna `ttpe` para `type`. |

---

## 📂 Subpasta: `schema/`

Uma sequência que ilustra a evolução técnica de um banco de dados, desde o rascunho até a implementação de regras de integridade.

| Arquivo | Foco em Integridade | Evolução do Esquema |
| :--- | :--- | :--- |
| `schema0.sql` | **Estrutura Básica** | Criação inicial de tabelas sem especificação de tipos de dados. |
| `schema1.sql` | **Afinidade de Tipos** | Introdução de tipos como `INTEGER` e `TEXT`. |
| `schema2.sql` | **Relacionamentos** | Implementação de `PRIMARY KEY` e `FOREIGN KEY`. |
| `schema3.sql` | **Unicidade** | Adição das restrições `UNIQUE` e `NOT NULL`. |
| `schema4.sql` | **Novo Modelo** | Reestruturação para incluir o sistema de cartões (`cards`) e passagens (`swipes`). |
| `schema5.sql` | **Refinamento** | Aplicação estrita de `NOT NULL` em campos essenciais. |
| `schema6.sql` | **Automação** | Uso de `DEFAULT CURRENT_TIMESTAMP` para preenchimento de data/hora. |
| `schema7.sql` | **Validação** | Introdução de `CHECK` para garantir que valores de `type` e `amount` sejam válidos. |

## 🛠️ Como Utilizar

Para criar a versão mais atualizada e segura do banco de dados, execute:

```bash
sqlite3 mbta.db < schema/schema7.sql
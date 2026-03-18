# Segurança e Administração de Sistemas - Módulo src6

Este diretório foca nos aspectos críticos de administração de bancos de dados, cobrindo desde o controle de acesso de usuários e permissões até a defesa contra ataques de injeção de SQL e o uso de procedimentos armazenados.

## 📂 Estrutura de Arquivos

Os scripts estão organizados por áreas de segurança e gerenciamento de banco de dados:

| Arquivo / Pasta | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `access/users.sql` | **User Management** | Criação e gerenciamento de contas de usuários no banco de dados. |
| `access/privileges.sql`| **DCL / Privileges** | Atribuição e revogação de permissões de acesso (GRANT/REVOKE). |
| `injection/injection.sql`| **SQL Injection** | Demonstração de vulnerabilidades de segurança em consultas não tratadas. |
| `injection/prepared.sql`| **Prepared Statements**| Uso de declarações preparadas como defesa contra ataques de injeção. |
| `mbta/load.sql` | **Data Loading** | Scripts para carga inicial de dados em massa no sistema de transporte. |
| `mbta/alter.sql` | **Schema Evolution** | Modificações e versionamento da estrutura de tabelas existentes. |
| `mfa/procedures.sql` | **Stored Procedures** | Automação de tarefas repetitivas através de procedimentos armazenados. |
| `mysql/` | **Client-Server SQL** | Transição para o ambiente MySQL, incluindo controles de acesso e defesa contra ataques específicos. |

## 🛡️ Segurança e Defesa

Este módulo destaca a importância de:
* **Princípio do Menor Privilégio**: Garantir que cada usuário tenha apenas as permissões necessárias para sua função.
* **Sanitização de Inputs**: Utilizar `prepared statements` para evitar a execução de código malicioso via formulários.
* **Encapsulamento**: Uso de `procedures` para proteger a lógica interna do banco de dados.

## 🛠️ Como Utilizar

Para configurar o esquema e carregar os dados do sistema MBTA:
```bash
sqlite3 mbta.db < mbta/schema.sql
sqlite3 mbta.db < mbta/load.sql
# Otimização e Concorrência - Módulo src5

Este diretório explora técnicas avançadas de performance através de indexação e garante a integridade dos dados em ambientes multiusuário através do controle de concorrência e transações.

## 📂 Subpasta: `concurrency/`

Focada em como o SQL lida com acessos simultâneos e garante que operações complexas sejam tratadas como uma única unidade.

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `transactions.sql` | **Transactions** | Uso de `BEGIN TRANSACTION` e `COMMIT` para garantir atomicidade. |
| `race_conditions.sql`| **Race Conditions** | Demonstração de conflitos que ocorrem quando múltiplos processos alteram o mesmo dado simultaneamente. |

---

## 📂 Subpastas: `index/` e `indexes/`

Estas pastas contêm scripts que demonstram como reduzir drasticamente o tempo de resposta de consultas em bases de dados de grande escala.

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `where.sql` | **B-Tree Index** | Criação de índices para acelerar filtragens em cláusulas `WHERE`. |
| `nested.sql` | **Nested Indexing** | Otimização de performance em subconsultas e buscas aninhadas. |
| `partial.sql` | **Partial Index** | Criação de índices que cobrem apenas uma parte da tabela para economizar espaço. |
| `vacuum.sql` | **Database Cleanup** | Uso do comando `VACUUM` para reconstruir o banco e liberar espaço em disco. |

## 💾 Bancos de Dados Utilizados

* **`bank.db`**: Simulação de sistema bancário para testes de transações e integridade.
* **`movies`**: Base de dados de grande escala utilizada para medir o ganho de performance com indexação.

## 🛠️ Como Utilizar

Para testar a segurança de uma transação:
```bash
sqlite3 bank.db < concurrency/transactions.sql
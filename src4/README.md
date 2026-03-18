# Visualizações e Segurança - Módulo src4

Este diretório foca no uso de **Views** (Visualizações) para simplificar consultas complexas, organizar dados de forma lógica e proteger informações sensíveis, além de implementar lógicas de exclusão suave.

## 📂 Estrutura de Arquivos

Os arquivos exploram como as visualizações podem transformar a interação com o banco de dados:

| Arquivo | Comando / Conceito | Descrição |
| :--- | :--- | :--- |
| `simplifying.sql` | **Simplificação** | Criação de Views para esconder a complexidade de múltiplos `JOINs`. |
| `aggregating.sql` | **Agregação** | Visualizações que consolidam cálculos e funções de agregação. |
| `securing.sql` | **Segurança** | Uso de Views para restringir o acesso a colunas ou registros sensíveis. |
| `partitioning.sql` | **Particionamento** | Divisão lógica de grandes tabelas em visualizações menores e específicas. |
| `soft_deletion.sql` | **Exclusão Lógica** | Implementação de Views que filtram automaticamente registros marcados como excluídos. |

## 💾 Bancos de Dados Utilizados

Nesta seção, as visualizações são aplicadas sobre diferentes contextos:
* `longlist.db`
* `mfa.db`
* `network.db`
* `rideshare.db`

## 🛠️ Como Utilizar

Para criar as visualizações definidas nos scripts no banco de dados correspondente, utilize:

```bash
sqlite3 mfa.db < simplifying.sql
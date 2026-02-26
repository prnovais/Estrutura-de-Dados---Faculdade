# Atividade de Banco de Dados - Comando UPDATE (DML)

Este repositório contém a resolução de uma atividade acadêmica da disciplina de Banco de Dados, do 3º semestre do curso de Análise e Desenvolvimento de Sistemas.

O objetivo era aplicar o comando `UPDATE` da linguagem SQL (DML) para alterar a localização de um produto em uma tabela, conforme enunciado fornecido pelo professor.

Enunciado: A partir da tabela `PRODUTOS` abaixo, elabore um comando DML que altere a **LOCALIZAÇÃO** do produto **Carnes** da **PRATELEIRA 3** para a **PRATELEIRA 4**.

Tabela: PRODUTOS
| ID | DESCRIÇÃO | LOCALIZAÇÃO   |
|----|-----------|---------------|
| 1  | Queijos   | PRATELEIRA 1  |
| 2  | Legumes   | PRATELEIRA 2  |
| 3  | Carnes    | PRATELEIRA 3  |
| 4  | Frutas    | PRATELEIRA 4  |
| 5  | Bebidas   | PRATELEIRA 5  |

Solução: Proposta
Foram elaboradas duas formas de resolver o problema, utilizando diferentes critérios no `WHERE`:

### Opção 1 (recomendada - usando a chave primária)
```sql
UPDATE PRODUTOS
SET LOCALIZAÇÃO = 'PRATELEIRA 4'
WHERE ID = 3;

UPDATE PRODUTOS
SET LOCALIZAÇÃO = 'PRATELEIRA 4'
WHERE DESCRIÇÃO = 'Carnes';

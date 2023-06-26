# MySQLFrameWork

- Este é um exemplo de como utilizar o MySQL em Python utilizando o pacote mysql-connector-python. O objetivo é automatizar e facilitar operações dentro de um ou mais banco de dados com o Sistema Gerenciador de Banco de Dados MySQL, como criar tabelas, inserir, atualizar e excluir dados de forma mais p´ratica, por exemplo, inserindo várias variáveis de forma mais prática.

## Pré-requisitos

- Para executar esse código é necessário ter instalado o Python e o pacote mysql-connector-python. Além disso, é preciso ter um servidor MySQL.

## Como utilizar

1 - Importe a biblioteca:
```python
import mysql.connector
```
2 - Crie uma conexão com o banco de dados. Adapte os dados de acesso em:
```python
HOST = 'localhost'
USER = 'root'
PASSWORD = '12345'
DATABASE = ''
```
3 - Crie uma instância da classe MySQLDB:
```python
db = MySQLDB()
```
4 - Execute as operações desejadas:
```python
# Criar tabela
db.create_table('clientes')

# Inserir dados
db.insert_data('clientes', '1, "João", "joao@gmail.com"')

# Selecionar dados
db.select_data('clientes', '*', 'id=1')

# Atualizar dados
db.update_data('clientes', 'email', 'joao@outlook.com', 'id=1')

# Excluir dados
db.delete_data('clientes', 'id=1')

# Adicionar coluna
db.add_column('clientes', 'idade', 'INT')

# Excluir tabela
db.drop_table('clientes')

# Fechar conexão
db.close_connection()
```

## Ferramentas

- MySQL
- Python

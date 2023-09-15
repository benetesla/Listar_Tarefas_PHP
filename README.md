
# Listar Tarefas PHP

Este é um aplicativo web de listagem de tarefas construído com PHP, JavaScript e Bootstrap, além de utilizar um banco de dados MySQL para armazenar as informações.

## Como Usar Esta Aplicação?

Para visualizar esta aplicação no frontend, é necessário ter o XAMPP instalado em sua máquina, juntamente com o Apache e o MySQL.

## Banco de Dados

Para utilizar todas as funcionalidades deste aplicativo, é necessário criar um banco de dados em sua máquina.

## Criação das Tabelas

Por favor, execute os seguintes códigos para criar as tabelas em seu banco de dados:

```sql
CREATE TABLE tb_status (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    status VARCHAR(25) NOT NULL
);

INSERT INTO tb_status(status) VALUES('pendente');
INSERT INTO tb_status(status) VALUES('realizado');

CREATE TABLE tb_tarefas (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    id_status INT NOT NULL DEFAULT 1,
    FOREIGN KEY (id_status) REFERENCES tb_status(id),
    tarefa TEXT NOT NULL,
    data_cadastrado DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP
);
```

## Criação do Banco de Dados

Lembre-se de criar um banco de dados para a conexão da aplicação.

### Cuidado com a Segurança

Esta aplicação foi construída com atenção à segurança. Certifique-se de separar os arquivos públicos dos privados para evitar possíveis invasões.


 

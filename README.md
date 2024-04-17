# SLQ_NODE

<PRE>

Passo 1: Instalação das Dependências
npm install mysql2
Passo 2: Código Node.js

    const mysql = require('mysql2');

    const connection = mysql.createConnection({
      host: 'localhost',
      user: 'g1',
      password: 'password',
      database: 'nome_do_seu_banco_de_dados'
    });

    connection.connect();

    const queryString = 'SELECT * FROM sua_tabela';

    connection.query(queryString, (error, results, fields) => {
      if (error) throw error;
      console.log('Resultado da consulta:');
      console.log(results);
    });

    connection.end();
  
Passo 3: Executando o Código
No terminal, navegue até o diretório onde você salvou o arquivo app.js e execute o seguinte comando:

node app.js

</PRE>

<PRE>

    // Suponha que você tenha uma variável chamada 'tableName' que contém o nome da tabela
const tableName = 'users';
// Suponha que você tenha uma variável chamada 'column' que contém o nome da coluna
const column = 'username';

// Construindo a query dinamicamente
const query = `SELECT ${column} FROM ${tableName} WHERE condition = 'some_condition';`;

// Em seguida, você pode usar essa query onde precisar
console.log(query);

</PRE>

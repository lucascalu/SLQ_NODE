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

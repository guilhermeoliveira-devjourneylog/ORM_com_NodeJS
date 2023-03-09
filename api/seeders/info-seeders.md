## demo-pessoa.js
Este é um arquivo de migração de banco de dados escrito em JavaScript usando a biblioteca Sequelize ORM para Node.js. O arquivo exporta duas funções: e , que são usadas para aplicar e desfazer a migração, respectivamente.updown

A função é responsável por adicionar novos dados ao banco de dados. Nesse caso, ele usa o método da queryInterface Sequelize para adicionar várias novas linhas à tabela. Cada linha representa uma pessoa, com propriedades para (nome), (status ativo), , (aluno ou professor) e carimbos de data/hora.upbulkInsertPessoasnomeativoemailrolecreatedAtupdatedAt

A função é responsável por desfazer as alterações feitas pela função. Nesse caso, ele usa o método de queryInterface para excluir todas as linhas da tabela.downupbulkDeletePessoas

Essas funções são usadas pela ferramenta Sequelize CLI para aplicar e desfazer a migração conforme necessário. Por exemplo, a execução aplicaria todas as migrações que ainda não foram aplicadas, incluindo esta. Por outro lado, a execução desfaria a migração mais recente, que seria esta se tivesse sido aplicada.npx sequelize-cli db:migratenpx sequelize-cli db:migrate:undo


## demo-nivel.js

Este é um arquivo de migração para semear a tabela "Niveis" no banco de dados usando o Sequelize.

A função define os dados a serem inseridos na tabela. Ele usa o método fornecido pelo objeto para inserir três objetos, cada um representando uma linha de dados, na tabela "Niveis". Os objetos têm uma propriedade, que indica o nível de proficiência de um curso, e propriedades que são geradas automaticamente por Sequelize.upbulkInsertqueryInterfacedescr_nivelcreatedAtupdatedAt

A função define como desfazer as alterações feitas pela função. Nesse caso, ele usa o método fornecido pelo objeto para excluir todas as linhas da tabela "Niveis".downupbulkDeletequeryInterface
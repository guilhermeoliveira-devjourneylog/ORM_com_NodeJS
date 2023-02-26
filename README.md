## node 
npm run start
npx sequelize-cli model:create --name Pessoas --attributes nome:string,ativo:boolean,email:string,role:string
npx sequelize-cli db:migrate
npx sequelize-cli seed:generate --name demo-pessoa
npx sequelize-cli db:seed:all

//Desfazendo operações
npx sequelize-cli db:migrate:undo

//Para desfazer uma migração específica. Nesse caso, lembre-se que só irá funcionar se não tiver nenhuma outra tabela relacionada a ela!
db:migrate:undo --name [data-hora]-create-[nome-da-tabela].js

//Desfazendo seeds Para desfazer o último seed feito.
npx sequelize db:seed:undo

//Para desfazer seeds de uma tabela específica.
npx sequelize-cli db:seed:undo --seed nome-do-arquivo

//Para desfazer todos os seeds feitos.
npx sequelize-cli db:seed:undo:all

## wsl
sudo service mysql status
sudo service mysql start
sudo mysql



CREATE USER 'nome_do_usuario'@'localhost' IDENTIFIED BY 'senha_do_usuario';
CREATE USER 'Developer'@'localhost' IDENTIFIED BY 'Dev-317297';

GRANT ALL PRIVILEGES ON *.* TO 'nome_do_usuario'@'localhost';
GRANT ALL PRIVILEGES ON *.* TO 'Developer'@'localhost';

FLUSH PRIVILEGES;

select user from mysql.user;

use escola_ingles;

show tables;

describe Pessoas;

 insert into Pessoas (nome, ativo, email, role, createdAt, updatedAt) values ("Leonidas Azmid", 1, "leonidasazmid@test.com", "estudante", NOW(), NOW());

select *from Pessoas;


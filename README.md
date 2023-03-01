## node 
```npm install sequelize sequelize-cli```
```npm init -y```
```npm run start```
```npm install mysql2```
```npm install sequelize```
```npm install sequelize sequelize-cli path```
```npx sequelize-cli init```
```npx sequelize-cli model:create --name Pessoas --attributes nome:string,ativo:boolean,email:string,role:string```
```npx sequelize-cli db:migrate```
```npx sequelize-cli seed:generate --name demo-pessoa```
```npx sequelize-cli db:seed:all```
```npx sequelize-cli model:create --name Niveis --attributes descr_nivel:string```
```npx sequelize-cli model:create --name Turmas --attributes data_inicio:dateonly```
```npx sequelize-cli model:create --name Matriculas --attributes status:string```
```npx sequelize-cli seed:generate --name demo-nivel```
```npx sequelize-cli seed:generate --name demo-turmas```
```npx sequelize-cli seed:generate --name demo-matriculas```
### Desfazendo operações
```npx sequelize-cli db:migrate:undo```

### Para desfazer uma migração específica. Nesse caso, lembre-se que só irá funcionar se não tiver nenhuma outra tabela relacionada a ela!
```db:migrate:undo --name [data-hora]-create-[nome-da-tabela].js```

### Desfazendo seeds Para desfazer o último seed feito.
```npx sequelize db:seed:undo```

### Para desfazer seeds de uma tabela específica.
```npx sequelize-cli db:seed:undo --seed nome-do-arquivo```

### Para desfazer todos os seeds feitos.
```npx sequelize-cli db:seed:undo:all```

## wsl
```mysql -u [usuário] -p```
```sudo mysql -u [usuário] -p```
```CREATE USER 'nome_do_usuario'@'localhost' IDENTIFIED BY 'senha_do_usuario';```
```GRANT ALL PRIVILEGES ON *.* TO 'nome_do_usuario'@'localhost';```
```FLUSH PRIVILEGES;```
```select user from mysql.user;```
```sudo apt install mysql-server```
```sudo service mysql status```
```sudo service mysql start```
```sudo mysql```
```show databases;```
```create database escola_ingles;```
```use escola_ingles;```
```show tables;```
```describe Pessoas;```
 ```insert into Pessoas (nome, ativo, email, role, createdAt, updatedAt) values ("Leonidas Azmid", 1, "leonidasazmid@test.com", "estudante", NOW(), NOW());```
```select *from Pessoas;```


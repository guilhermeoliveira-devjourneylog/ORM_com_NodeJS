## PessoaController.js

Este é um módulo Node.js que exporta uma classe chamada PessoaController. 
A classe tem vários métodos estáticos que definem as rotas e a lógica para manipular solicitações HTTP para um servidor. PessoaController 

Os métodos são: 

pegaPessoasAtivas: retorna todas as pessoas ativas de uma tabela de banco de dados. 

pegaTodasAsPessoas: retorna todas as pessoas de uma tabela de banco de dados. 

pegaPessoa: retorna uma única pessoa identificada por um parâmetro na URL da solicitação.id 

criaPessoa: cria uma nova pessoa com base nos dados JSON enviados no corpo da solicitação. 

atualizaPessoa: atualiza uma pessoa existente identificada por um parâmetro na URL da solicitação, com base nos dados JSON enviados no corpo da solicitação.id 

apagaPessoa: exclui uma pessoa existente identificada por um parâmetro na URL da solicitação.id 

restauraPessoa: restaura uma pessoa existente que foi excluída anteriormente, identificada por um parâmetro na URL da solicitação.id 

pegaMatriculas: retorna todas as inscrições associadas a um aluno específico, identificadas por um parâmetro na URL da solicitação.estudanteId 

cancelaPessoa: cancela todas as inscrições associadas a um aluno específico, identificado por um parâmetro na URL da solicitação.estudanteId 

Os métodos usam uma instância da classe para manipular a lógica de negócios e as interações com o banco de dados. O módulo exporta a classe para que ela possa ser usada em outras partes de um aplicativo Node.js.PessoasServicesPessoaController 

## NivelController.js

Este é um módulo controlador Node.js para gerenciar objetos Nivel. Ele exporta um objeto que contém vários métodos assíncronos estáticos: 

pegaTodosOsNiveis: recupera todos os objetos Nivel do banco de dados e os retorna em uma resposta JSON. 

pegaNivel: recupera um único objeto Nivel por seu ID e o retorna em uma resposta JSON. 

criaNivel: cria um novo objeto Nivel no banco de dados e o retorna em uma resposta JSON. 

atualizaNivel: atualiza um objeto Nivel existente no banco de dados com novas informações e retorna uma mensagem de êxito em uma resposta JSON. 

apagaNivel: exclui um objeto Nivel do banco de dados e retorna uma mensagem de êxito em uma resposta JSON. 

restauraNivel: restaura um objeto Nivel excluído anteriormente no banco de dados e retorna uma mensagem de êxito em uma resposta JSON. 

Os métodos usam uma instância da classe, que é responsável por manipular as interações de banco de dados. A classe é instanciada com um parâmetro que representa o nome da tabela no banco de dados que corresponde aos objetos Nivel. Services Services 

Os métodos retornam respostas JSON com o(s) objeto(s) solicitado(s) ou uma mensagem de erro se a solicitação falhar. Os códigos de status HTTP usados são 200 para solicitações bem-sucedidas e 500 para solicitações com falha. 

## TurmaController.js

Este é um módulo controlador Node.js que exporta um objeto com vários métodos para manipular solicitações HTTP relacionadas a recursos. Turma 

O módulo requer o módulo do mesmo diretório para fornecer acesso à lógica de negócios relacionada aos recursos do Turma .TurmaController TurmasServices 

As exportações seis métodos:TurmaController 

pegaTodasAsTurmas: manipula solicitações GET para todos os recursos Turmas, opcionalmente filtrando-as por intervalo de datas usando parâmetros de consulta. 

pegaTurma: manipula solicitações GET para um único recurso da Turma identificado por seu parâmetro.id 

criaTurma: lida com solicitações POST para criar novos recursos do Turma . 

atualizaTurma: manipula solicitações PUT para atualizar um recurso da Turma identificado por seu parâmetro.id 

apagaTurma: manipula solicitações DELETE para excluir um recurso da Turma identificado por seu parâmetro.id 

restauraTurma: manipula solicitações PATCH para restaurar um recurso Turma excluído identificado por seu parâmetro.id 

Cada método tem tratamento de erros e retorna um objeto de resposta HTTP com um código de status apropriado e uma carga JSON que representa os dados solicitados ou a mensagem de erro. 

## MatriculaController.js 

Este é um módulo Node.js que exporta uma classe chamada MatriculaController. A classe tem vários métodos estáticos que lidam com solicitações HTTP e respostas relacionadas às matrículas dos alunos. A classe usa o ORM Sequelize para interagir com um banco de dados e fornece a funcionalidade CRUD (Create, Read, Update, Delete) para matrículas de alunos. MatriculaController 

Aqui está uma breve visão geral de cada método: 

pegaUmaMatricula: Localiza e retorna um único registro de matrícula de aluno com base na ID de aluno e na ID de matrícula fornecidas nos parâmetros de solicitação. 

criaMatricula: Cria um novo registro de matrícula de aluno para a ID de aluno fornecida nos parâmetros de solicitação usando os dados fornecidos no corpo da solicitação. 

atualizaMatricula: Atualiza um registro de matrícula de aluno existente para a ID de estudante e a ID de matrícula fornecidas nos parâmetros de solicitação usando os dados fornecidos no corpo da solicitação. 

apagaMatricula: Exclui um registro de matrícula de aluno existente para a ID de inscrição fornecida nos parâmetros de solicitação. 

restauraMatricula: Restaura um registro de matrícula de aluno excluído para a ID de inscrição fornecida nos parâmetros de solicitação. 

pegaMatriculasPorTurma: Localiza e retorna todos os registros de matrícula do aluno para o ID da classe fornecido nos parâmetros de solicitação que têm um status de 'confirmado'. 

pegaTurmasLotadas: Localiza e retorna o número de turmas que têm pelo menos 2 matrículas de alunos confirmadas. 

 
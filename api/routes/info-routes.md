## index.js

Esta é uma instrução module.exports para um módulo Node.js que exporta uma função que configura o middleware para lidar com solicitações HTTP em um aplicativo Express.js.

O módulo importa o middleware "body-parser", que é usado para analisar corpos de solicitação de entrada no formato JSON e módulos de rota para "pessoas", "niveis" e "turmas".

A função exportada usa uma instância "app" .js Express como um argumento e chama três métodos nela: "use", "pessoas", "niveis" e "turmas".

O método "use" é usado para montar funções de middleware na cadeia de middleware. Nesse caso, ele é usado para montar o middleware "body-parser.json()", que analisa solicitações JSON de entrada.

Os módulos de rota "pessoas", "niveis" e "turmas" são então montados no aplicativo usando o mesmo método de "uso". Esses módulos de rota definem os endpoints para os recursos "pessoas", "niveis" e "turmas" e lidam com solicitações HTTP de entrada para esses endpoints. Ao montar esses módulos de rota no aplicativo, a cadeia de middleware é estendida para incluir os manipuladores definidos nesses módulos para os pontos de extremidade correspondentes.

## pessoasRoute.js

Esta é uma instrução module.exports para um módulo Node.js que exporta um roteador Express.js. O roteador define os pontos de extremidade para o recurso "Pessoas" e lida com solicitações HTTP de entrada para esses pontos de extremidade.

O módulo importa a classe "Router" do módulo "express", bem como os módulos "PessoaController" e "MatriculaController", que definem a lógica para lidar com as solicitações HTTP para o recurso "Pessoas".

O roteador exportado é definido usando a classe "Router" e os métodos ".get()", ".post()", ".put()" e ".delete()" para definir os vários pontos de extremidade do recurso.

Por exemplo, ".get('/pessoas', PessoaController.pegaTodasAsPessoas)" configura um ponto de extremidade GET para a rota "/pessoas", que chama o método "pegaTodasAsPessoas()" do "PessoaController" quando o endpoint é solicitado.

Da mesma forma, ".post('/pessoas', PessoaController.criaPessoa)" configura um ponto de extremidade POST para a rota "/pessoas", que chama o método "criaPessoa()" do "PessoaController" quando o endpoint é solicitado.

Os vários endpoints definidos no roteador correspondem às operações CRUD para o recurso "Pessoas", bem como operações adicionais relacionadas à criação e gerenciamento de "Matriculas" (matrículas).


## niveisRoute.js

Essas rotas definem os pontos de extremidade da API para o recurso "Níveis". Eles mapeiam métodos HTTP para métodos de controlador, permitindo que os clientes interajam com o recurso.

Aqui estão as explicações para cada ponto de extremidade:

GET : Recupera uma lista de todos os níveis./niveis
GET : Recupera um nível específico por sua ID./niveis/:id
POST : Cria um novo nível./niveis
POST : Restaura um nível excluído anteriormente./niveis/:id/restaura
PUT : Atualiza um nível específico por sua ID./niveis/:id
DELETE: Exclui um nível específico por sua ID./niveis/:id

## turmasRoute.js

Esse código parece definir um roteador para lidar com solicitações HTTP relacionadas à entidade. Os pontos de extremidade disponíveis são:Turma

GET /turmas: recupera todas as instânciasTurma
GET /turmas/:id: recupera uma instância específica por IDTurma
POST /turmas: cria uma nova instânciaTurma
POST /turmas/:id/restaura: restaura uma instância excluída anteriormenteTurma
PUT /turmas/:id: atualiza uma instância específica por IDTurma
DELETE /turmas/:id: exclui uma instância específica por IDTurma
Parece que o roteador usa a para lidar com as solicitações.TurmaController
# Programação de Funcionalidades

## Requisitos Atendidos

As tabelas que se seguem apresentam os requisitos funcionais e não-funcionais que relacionam o escopo do projeto com os artefatos criados:

### Requisitos Funcionais

| ID     | Descrição do Requisito                                                                                                                                           | Prioridade | Artefato Criado                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------|
| RF-001 | A aplicação deve permitir que os alunos sejam cadastrados pelos ADMs(instrutores).| ALTA       | [pagina cadastrar] / [pagina cadastrar 2]                                   |
|RF-002| A aplicação deve fornecer um sistema de autenticação seguro, permitindo que os alunos acessem suas contas por meio de um processo de login. | ALTA | [area de login] |
|RF-003| A aplicação deve oferecer um processo de recuperação de senha, permitindo que usuários redefinam suas senhas em caso de esquecimento ou perda. | ALTA | [pagina recuperar senha] |
|RF-004| A aplicação deve apresentar uma página exclusiva para cada aluno, contendo informações sobre o nivel e últimas informações. | ALTA | [pagina-do-aluno] |
| RF-005 | A aplicação deve permitir que os alunos gerenciem suas informações de perfil (alterar, excluir e consultar os dados) a qualquer momento.                           | ALTA       | [pagina cadastrar] / [pagina cadastrar 2]                                   |
| RF-006 | A aplicação deve possibilitar que as ADMs(instrutores) divulguem eventos, editem e criem conteudo para os diversos níveis do sistema.   | ALTA       | [administracao]/ [novo evento] / [conteudo do nivel]                                                        |
| RF-007 | Os alunos devem poder indicar seu interesse e disponibilidade para eventos.   | ALTA       | [eventos]                                                     |
| RF-008 | A aplicação deve permitir que os ADMs marquem eventos como concluídos ou encerrados.   | ALTA       | [eventos]                                                     |
| RF-009 | A aplicação deve apresentar página contendo informações da escola.   | ALTA       | index.html                                                      |
| RF-010 | A aplicação deve apresentar página contendo informações referente aos certificados, como pesquisa pelo codigo do certificado.   | ALTA       | [validar certificado]                                                      |
| RF-011 | A aplicação deve apresentar a página “Como Começar” que orienta os visitantes sobre os passos necessários para se tornarem alunos registrados na aplicação. | ALTA       | como-comecar.html                                                             |
| RF-012 | Deve existir uma página inicial (landing page) informativa que apresenta o propósito da plataforma e incentiva tanto os visitantes quanto os alunos a utilizar a aplicação. | ALTA       | index.html                                                             |
| RF-013 | A aplicação deve conter a página “Perguntas Frequentes” que aborda as dúvidas mais comuns dos visitantes em relação a escola e ao uso da plataforma. | ALTA       | perguntas-frequentes.html                                                             |
| RF-014 | A aplicação deve apresentar a página “Por Que Se matricular?” que apresenta os benefícios pessoais que podem ser obtidos ao se tornar aluno. | ALTA       | por-que-se-matricular.html                                                     |
| RF-015 | A aplicação deve apresentar a página “Histórias de Sucesso” que destaca projetos anteriores realizados por meio da plataforma, com resultados, depoimentos de voluntários e o impacto positivo alcançado. | ALTA       | historias-de-sucesso.html                                                     |
| RF-016 | Os alunos devem receber um e-mail quando a um novo evento cadastrado. | MÉDIA       | [eventos] |
| RF-017 | A página do nivel admnistrado pelos ADMs deve exibir uma lista de todos os alunos que estão no nivel informado. | BAIXA       | [administracao de nivel] |
| RF-018 | Na página de evento cadastrada pelos ADMs, deve ter um botão com a finalidade de enviar um link via e-mail aos voluntários solicitando a eles entrem em contato informando a participação ou não dos eventos. | BAIXA       | [eventos] |



## Descrição das estruturas:
## Aluno
|   **Nome**    | **Tipo**         | **Descrição**                              | **Exemplo**                                       |
|:-------------:|------------------|--------------------------------------------|---------------------------------------------------|
|      Id       | Number             | Identificador único do aluno           | 1              |
| Id do nivel | Number             | Identificador único do nivel relacionada | 1              |
|     Nome      | Texto            | Nome do aluno                          | João                                              |
|     Email     | Texto            | Endereço de e-mail do aluno            | joao@email.com                                    |
|     CPF     | Number            | Número do cadastro de pessoa física            | 123.456.78-90                                    |
|     Telefone     | Number            | Número de contato do aluno            | (47) 9 8765-4321                                    |
|   Senha   | Texto(SHA-256) | Senha de acesso à conta do aluno                           | bdcebd4f01d7024696ba685eefc1c5dd446071b0c89f858aae7ef136c439e09e |
|    CEP    | Texto          | Código de Endereçamento Postal (CEP)                     | 30170131                                                         |
|    Rua    | Texto          | Nome da rua onde está localizada a ONG                   | Rua dos Tupis                                                    |
|  Número   | Texto          | Número do endereço da ONG                                | 646                                                              |
|  Cidade   | Texto          | Cidade onde está localizada a ONG                        | Belo Horizonte                                                   |
|  Estado   | Texto          | Abreviação do estado onde está localizada a ONG          | MG (ISO 3166-2: BR)                                              |
|  Imagem   | Texto          | Texto representando a imagem da ONG convertida em base64 | `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEFFAUUAAD/...`         |
|    status     | texto          | Status do nivel  | "Pendente", "Aprovado", "Concluido"                                  |
|     Momento de Criação      | Timestamp | Data e hora de cadastro | "2023-03-27T03:05:18.345Z"            |
|     cadastrado por      | Texto | nome do ADM que criou o cadastro | "João"            |
|     ADMIN      | Boolean | booleano informando o estado de administrador | TRUE, FALSE            |
|

## Nivel do sistema
|      **Nome**      | **Tipo**  | **Descrição**                                           | **Exemplo**                          |
|:------------------:|-----------|---------------------------------------------------------|--------------------------------------|
|         Id         | NUMBER      | Identificador único do nivel                       | 1 |
|     Nome      | Texto            | Nome do nivel                          | "SIU NIM TAO"                                              |
|

## Sessão
| **Nome**  | **Tipo**  | **Descrição**                                       | **Exemplo**                      |
|:---------:|-----------|-----------------------------------------------------|----------------------------------|
|    Id     | Number    | Identificador único da sessão                       | 123                            |
| Id do aluno | Number    | Identificador único do aluno                          | 234                             |
|   token   | Texto     | Token que é verificado a cada request se esta ativo | e10adc3949ba59abbe56e057f20f883e |
| expiração | Timestamp | Data e hora limite em que a sessão ficará ativa     | 2023-10-28T22:41:38+00:00        |
|  active   | Boolean   | Data e hora limite em que a sessão ficará ativa     | 2023-10-28T22:41:38+00:00        |

# Especificações do Projeto

Pensando em como os alunos e instrutores de Wing Chun podem aprimorar a organização e administração das atividades da escola, está sendo criada esta aplicação com o principal foco em conectar esses indivíduos com a GONDAS Wing Chun.

No processo de planejamento do projeto foram utilizados os seguintes passos: definição das personas mais coerentes para a aplicação, mapeamento das necessidades e dores dos usuários e a criação dos requisitos que norteiam e definem o desenvolvimento do projeto.

Com os dados abaixo levantados será possível a elaboração da aplicação, cujo intuito é atender as demandas da GONDAS Wing Chun, facilitando a gestão de alunos e eventos e aplicando os conhecimentos na área de tecnologia


## Personas
### Elisa Marques
<img src="./img/personas/persona-elisa-marques.jpg" alt="Persona Elisa Marques" width="300"/>

Uma Administradora de 32 anos dedicada que vive na correria do dia a dia, tem interesse em praticar algum esporte ou alguma academia mas não sabe por onde começar, tem interesses em defesa pessoal, precisa de informações solídas para se decidir e suporte para continuar.
### Gustavo Silva
<img src="./img/personas/persona-gustavo-silva.jpg" alt="Persona Gustavo Silva" width="300"/>

Um calouro do curso de ED Fisica de 22 anos que cresceu assistindo filmes de kung fu e se apaixonou pelas artes marciais, praticante de Wing Chun a 4 anos hoje está vivenciando o 3º nível do sistema mas esta com dificuldade de encontrar tempo para treinar.

### Heitor Santos
<img src="./img/personas/persona-heitor-santos.jpg" alt="Persona Heitor Santos" width="300"/>

Um empresario local de 48 anos que gosta de viajar nos tempos livres, é praticante de Wing Chun a 12 anos e quando pode ajuda na organização da escola a qual faz parte, atualmente vivencia o 5º nível do sistema e gostaria de poder ajudar mais seu Sifu.

## Histórias de Usuários

Com base na análise das personas forma identificadas as seguintes histórias de usuários:

|EU COMO... `PERSONA`| QUERO/PRECISO ... `FUNCIONALIDADE` |PARA ... `MOTIVO/VALOR`                 |
|--------------------|------------------------------------|----------------------------------------|
|Elisa Marques  | Quero me cadastrar para ser aluna em uma escola de defesa pessoal. | Aprender a se defender e ao mesmo tempo sair do sedentarismo. |
|Elisa Marques      | Quero saber dos eventos que batem com meu interesse e minha disponibilidade.                | Para poder participar e me organizar com maior flexibilidade.|
|Gustavo Silva  | Saber informações sobre meu nível como forma e aplicações. | Poder poder aprender, progredir e ter maior acompanhamento dentro do sistema. |
|Gustavo Silva       | Consultar informações sobre seus certificados.                  | Para poder apresentar na faculdade e ganhar horas ACG (atividades Complementares de Graduação). |
|Heitor Santos       | Ajudar na organização dos eventos e a cadastrar novos alunos.        | Para que assim tenha maior padronização e agilidade nas informações melhorando a organização da escola.|              |

## Programação de Funcionalidades

### Requisitos Funcionais

| ID     | Descrição do Requisito                                                                                                                                           | Prioridade | Tipo       |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|------------|
| RF-001 | A aplicação deve permitir que os alunos sejam cadastrados pelos ADMs (instrutores).                                                                              | ALTA       | Dinâmico   |
| RF-002 | A aplicação deve fornecer um sistema de autenticação seguro, permitindo que os alunos acessem suas contas por meio de um processo de login.                       | ALTA       | Dinâmico   |
| RF-003 | A aplicação deve oferecer um processo de recuperação de senha, permitindo que usuários redefinam suas senhas em caso de esquecimento ou perda.                    | ALTA       | Dinâmico   |
| RF-004 | A aplicação deve apresentar uma página exclusiva para cada aluno, contendo informações sobre o nível e últimas informações.                                       | ALTA       | Dinâmico   |
| RF-005 | A aplicação deve permitir que os alunos gerenciem suas informações de perfil (alterar, excluir e consultar os dados) a qualquer momento.                          | ALTA       | Dinâmico   |
| RF-006 | A aplicação deve possibilitar que os ADMs (instrutores) divulguem eventos, editem e criem conteúdo para os diversos níveis do sistema.                           | ALTA       | Dinâmico   |
| RF-007 | Os alunos devem poder indicar seu interesse e disponibilidade para eventos.                                                                                      | ALTA       | Dinâmico   |
| RF-008 | A aplicação deve permitir que os ADMs marquem eventos como concluídos ou encerrados.                                                                             | ALTA       | Dinâmico   |
| RF-009 | A aplicação deve apresentar página contendo informações da escola.                                                                                               | ALTA       | Estático   |
| RF-010 | A aplicação deve permitir que ADMs adicionem, editem ou excluam certificados quando necessario                                                                                               | ALTA       | Estático   |
| RF-011 | A aplicação deve apresentar página contendo informações referentes aos certificados, permitindo que sejam pesquisado e visualizado por qualquer um com o codigo. | ALTA       | Estático   |
| RF-012 | A aplicação deve incluir um campo para upload de imagem para que o ADM adcione cada certificado, permitindo que uma representação visual seja acessada durante a busca.| ALTA       | Dinâmico   |
| RF-013 | Os alunos autenticados devem poder baixar o certificado em formato PDF, limitado aos certificados associados ao seu ID de aluno.                                  | Baixa       | Dinâmico   |
| RF-014 | A aplicação deve apresentar a página “Como Começar” que orienta os visitantes sobre os passos necessários para se tornarem alunos registrados na aplicação.       | ALTA       | Estático   |
| RF-015 | Deve existir uma página inicial (landing page) informativa que apresenta o propósito da escola e incentiva tanto os visitantes quanto os alunos a utilizar a aplicação. | ALTA       | Estático   |
| RF-016 | A aplicação deve conter a página “Perguntas Frequentes” que aborda as dúvidas mais comuns dos visitantes em relação à escola e ao uso da plataforma.               | ALTA       | Estático   |
| RF-017 | A aplicação deve apresentar a página “Por Que Se Matricular?” que apresenta os benefícios pessoais que podem ser obtidos ao se tornar aluno.                      | ALTA       | Estático   |
| RF-018 | A aplicação deve apresentar a página “Histórias de Sucesso” que destaca realizações anteriores, com depoimentos de alunos e o impacto positivo alcançado.         | ALTA       | Estático   |
| RF-019 | Os alunos devem receber um e-mail quando um novo evento for cadastrado.                                                                                          | MÉDIA      | Dinâmico   |
| RF-020 | A página do nível administrado pelos ADMs deve exibir uma lista de todos os alunos que estão no nível informado.                                                  | BAIXA      | Dinâmico   |
|

### Requisitos não Funcionais

| ID      | Descrição do Requisito                                                                                           | Prioridade |
|---------|------------------------------------------------------------------------------------------------------------------|------------|
| RNF-001 | A aplicação deve oferecer uma interface com design responsivo que se adapte aos dispositivos móveis e desktops.  | ALTA       |
| RNF-002 | A aplicação deve apresentar um layout simples e de fácil utilização.                                              | ALTA       |
| RNF-003 | As senhas dos usuários devem ser criptografadas antes de serem armazenadas.                                       | ALTA       |
| RNF-004 | A aplicação deve fornecer feedback visual claro para ações do usuário, como confirmações de envio e mensagens de erro. | ALTA       |
| RNF-005 | O sistema deve ser capaz de ser executado nas versões mais recentes dos principais navegadores do mercado, como Chrome, Firefox, Edge e Safari. | ALTA       |
| RNF-006 | A aplicação deve garantir que as imagens dos certificados sejam armazenadas de forma segura e acessíveis para visualização. | ALTA       |
| RNF-007 | Os certificados em formato PDF devem ser disponibilizados para download apenas para alunos autenticados, com base no ID do aluno associado ao certificado. | ALTA       |

### Restrições

| ID  | Restrição                                                                                                              |
|-----|------------------------------------------------------------------------------------------------------------------------|
| 01  | Não será possível efetuar pagamentos pelo site.                                                                        |
| 02  | Cada aluno poderá cadastrar no máximo 1 conta por CPF.                                                                 |
| 04  | A comunicação entre alunos e ADMs ocorrerá de forma externa à aplicação (e-mail, telefone, mensagens de texto).        |

# Ponderada-de-MVC

Nome do Projeto: Abandono 0
Descrição: O INSPA está criando um projeto cujo objetivo é entender os motivos do abandono de animais. Para isso, será desenvolvido um site com integração à banco de dados para coletar informações de usuários no geral, desde pessoas que têm, tiveram, terão ou nunca teriam cachorros, com essas informações, será feito um relatório para que os pesquisadores possam concluir os motivos do abandono.
Arquitetura: MVC (Model-View-Controller)
Ferramenta de Diagramação: Draw.io

Modelos (Models):

&nbsp;&nbsp;&nbsp;&nbsp;O Model é responsável por manipular os dados. Dessa forma, as informações emitidas pelo usuário são controladas e são guardadas informações como:
* ID do usuário (Garante que o usuário responde o formulário apenas uma vez)
* Nome do usuário (opcional)
* Senha do usuário (Permite que o usuário tenha uma conta e entre ou saia quando quiser)
* Tabela de dados (Respostas do usuário são armazenadas de forma organizada)
* Relatório (O pesquisador tem acesso a um relatório detalhado sobre as informações obtidas)
* Respostas dos formulários
&nbsp;&nbsp;&nbsp;&nbsp;Assim, todas essas informações são enviadas e ficam registradas no banco de dados, tornando-se de livre acesso ao pesquisador.

Controladores (Controllers):

&nbsp;&nbsp;&nbsp;&nbsp;Os controllers são responsáveis por gerenciar as interações entre o Model e a View. Eles interpretam as requisições do usuário e coordenam as operações necessárias nos Models, antes de enviar os dados processados para a View.
O projeto foi dividido em 3 controllers, são eles:
* Users: Realiza as operações após as ações do usuário, como gravar as informações emitidas (cadastro ou login) e, ao mesmo tempo, validá-las. Então, as informações de cadastro e login chegam ao controller, essas informações são validadas e enviadas ao banco de dados.
* Pesquisador: Realiza operações após as ações do pesquisador, como finalizar o processo ou filtrar informações. Então, o controller percebe quando os botões de filtro ou finalização são acionados e realizam essas ações.
* Informações: Realiza operações após as ações do usuário dentro do formulário, dessa forma, as respostas são gravadas e a passagem de pergunta é validada. Então, o controller recebe as respostas do formulário e, logo depois, as envia para o Model, que grava no banco de dados.

Views (Views):

&nbsp;&nbsp;&nbsp;&nbsp;O view tem todas as páginas que serão visualizadas pelo usuário, a princípio, desenvolvemos alguns elementos importantes para a construção do site, e variam a depender de qual página o usuário está, mas no geral são eles:
* Texto introdutório (Explicação geral do que é o projeto)
* Botão de cadastro/login
* Imagens
* Home
* Sobre
* Contatos (links, e-mails e relatório detalhado)
* Botão de finalizar
* Tabela de informações
* Botão de filtro
* Perguntas
* Caixa de respostas
* Botão de próxima/anterior pergunta
* Botões de perfil (O usuário seleciona qual o seu perfil para responder os próximos formulários, esses perfis variam de pessoas que nunca tiveram cães, tem ou não querem ter)

&nbsp;&nbsp;&nbsp;&nbsp;Essas informações vão sendo disponibilizadas ao decorrer das ações dentro do site. Entretanto, temos dois tipos de usuários, por isso, nenhum deles verá todas as telas, visto que cada um tem uma funcionalidade específica dentro da pesquisa, como o pesquisador que acessa os dados e o usuário comum, que fornece os dados.

Infraestrutura:

&nbsp;&nbsp;&nbsp;&nbsp;Inicialmente o projeto conta com o sistema de gerenciamento de banco de dados relacional chamado PostgreeSQL, esse banco de dados vai ser responsável por armazenar as tabelas com as respostas. Além disso, o MVC está presente no Model, dessa forma, ele nunca será acessado pelo usuário, apenas o pesquisador terá acesso a esses dados ao final.

Implicações da Arquitetura

&nbsp;&nbsp;&nbsp;&nbsp;A utilização do Sails.js permite o desenvolvimento mais rápido detalhado de aplicativos web e API’s. Com isso, a separação de camadas de software é melhor feita, o que permite um maior entendimento da aplicação.
&nbsp;&nbsp;&nbsp;&nbsp;As tecnologias utilizadas também permitem uma maior escalabilidade, já que a divisão é feita em camadas, o que permite também a manutenção do código, que pode ser organizada e testada individualmente. 

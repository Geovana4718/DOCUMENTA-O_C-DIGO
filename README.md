# DOCUMENTAÇÃO 

## Sistema de Reserva de Salas ##

Este é um sistema desenvolvido para gerenciar a reserva de salas em um ambiente corporativo. O objetivo principal é permitir que os usuários reservem, visualizem e cancelem reservas de salas de forma eficiente e sem conflitos de agendamento.

O sistema foi projetado para ser simples de usar e gerenciar, com funcionalidades para adicionar novas salas, fazer reservas para horários específicos, verificar a disponibilidade das salas e listar as reservas realizadas.

## Objetivo ##

O sistema visa resolver problemas comuns em ambientes corporativos, como:
- Gerenciar a disponibilidade de salas de aula.
- Permitir aos usuários reservar salas de forma rápida e sem conflitos.
- Oferecer uma maneira simples de listar as salas e reservas existentes.
- Garantir que as reservas não se sobreponham.

 ## Funcionalidades ##

 **Login:** Administradores e porteiros podem se autenticar no sistema.
 
**Cadastro de funcionário:** COPED será responsável pelo cadastro dos professores no sistema.

**Cadastro de Sala:** COPED será responsável pelo cadastro de todas as salas da instituição.

**Remover chave:** Em caso de uma sala estar indisponivel por um long período de tempo por questões de funcionaidade.

**Cadastrar reserva:** Porteiros podem emprestar chaves para os professores com reservas confirmadas.

**Devolução de Chave:** Porteiros registram a devolução das chaves emprestadas.

**Visualização de Reservas:** Professores e porteiros podem visualizar as reservas feitas.

**Fechar reservas:** Assim que o colaborador terminar de ultilizar, o porteiro fecha e encerra a reserva.

**Gerenciamento de Salas:** Administradores podem visualizar, adicionar e remover salas.

## Ferramentas e Tecnologias Utilizadas ##

- **Linguagem de Programação**: Java (versão 17).
- **IDE**: NETBEANS.
- **Controle de Versão**: Git, com repositório no GitHub.
- **Banco de Dados**: PostgreSQL.
- **Bibliotecas**: Para manipulação de datas e horários.

# Estrutura do Projeto com MVC

O projeto segue a arquitetura MVC (Model-View-Controller), que separa a aplicação em três componentes principais: Model, View e Controller. A seguir, vamos detalhar as classes dentro de cada uma dessas camadas.

## Model 
O Model é responsável pela lógica do negócio e manipulação de dados. Ele contém as classes que representam as entidades do sistema, como Chave, Funcionario, Reserva, etc.

**Chave.java:** Classe que representa as chaves das salas. Contém informações sobre o estado da chave (se está disponível ou não) e o relacionamento com a sala a qual pertence.

**Funcionario.java:** Classe que representa os funcionários que podem fazer reservas ou interagir com as salas. Ela armazena informações como nome, matrícula e outros dados relevantes para a gestão do sistema de reservas.

**Reserva.java:** Classe que representa uma reserva feita por um funcionário. Ela armazena os dados da reserva, como a sala, o horário da reserva e o usuário responsável. É uma das principais entidades do sistema.

**ReservaDetalhe.java:** Classe que contém os detalhes de uma reserva, como a data e horário específico, o turno (manhã, tarde, noite).

**Selecao.java:** Classe que gerencia as seleções de salas e turnos disponíveis para as reservas. Ela ajuda a selecionar quais salas estão livres em determinado horário e facilita a consulta das opções de reservas.

**Usuario.java:** Classe que representa os usuários do sistema (como porteiros e membros da COPED). Ela armazena dados sobre o tipo de usuário (se é COPED ou porteiro) e o acesso que cada tipo de usuário tem no sistema.

## View
A View é responsável pela interface com o usuário, exibindo as informações e permitindo que o usuário interaja com o sistema.

**Menu.java:** Classe responsável pela exibição do menu principal. Ela fornece uma interface para o usuário navegar entre as opções do sistema, como fazer uma reserva, visualizar reservas ou acessar configurações.

**MenuCOPED.java:** Classe que exibe o menu específico para a equipe da COPED. Ela oferece opções relacionadas às funcionalidades que a COPED precisa utilizar, como cadastro de funcionários e salas.

**TelaReserva.java:** Classe responsável pela interface onde o usuário pode realizar as reservas de salas. Ela permite que o usuário selecione a sala, o horário e o turno, e finalize a reserva.

**LoginTela.java:** Classe que exibe a tela de login, onde os usuários (porteiros e membros da COPED) podem inserir suas credenciais para acessar o sistema. Ela valida as informações do usuário e redireciona para a interface correta dependendo do tipo de usuário.

## Controller
O Controller é responsável pela lógica de controle, gerenciando as interações entre a View e o Model. Ele manipula as entradas do usuário e atualiza o Model ou a View conforme necessário.

**ChaveController.java:** Controlador responsável por gerenciar as operações relacionadas à classe Chave. Ele pode lidar com a entrega e devolução das chaves, garantindo que as salas sejam acessadas de acordo com as reservas.

**Conexao.java:** Classe responsável por gerenciar a conexão com o banco de dados (ou outro sistema de armazenamento de dados). Ela é fundamental para garantir que as operações de leitura e escrita no banco de dados sejam feitas corretamente.

**FuncionarioController.java:** Controlador responsável pelas operações relacionadas aos Funcionários, como registrar um novo funcionário, visualizar suas informações e realizar interações específicas com as reservas.

**ReservaController.java:** Controlador responsável pela manipulação das reservas. Ele gerencia a criação, modificação e cancelamento de reservas, interagindo com o Model e a View para garantir que as operações sejam realizadas corretamente.

**SelecaoController.java:** Controlador responsável pela lógica de seleção das salas e turnos disponíveis. Ele consulta o Model para verificar a disponibilidade das salas e fornece as opções para o usuário.

## Main
A classe Main é o ponto de entrada do sistema. Ela inicializa o aplicativo e coordena a interação entre as diferentes partes do sistema.

**ReservaDeSala.java:** Classe principal que inicializa o sistema e coordena a execução do projeto. Ela cria as instâncias das Views, Controllers e Models, e garante que o fluxo de execução do sistema ocorra de maneira adequada.

## Conclusão ##

O sistema de reserva de salas foi desenvolvido com sucesso, permitindo o gerenciamento de salas e a realização de reservas sem conflitos. No entanto, o sistema pode ser expandido para incluir recursos adicionais, como integração com calendários, autenticação de usuários e persistência de dados em banco de dados.

Com as ferramentas utilizadas, conseguimos desenvolver uma solução simples, eficiente e fácil de usar, que pode ser melhorada conforme necessário para atender a diferentes cenários de uso.


























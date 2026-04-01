# Atividade Avaliativa
Projeto Flutter com Splash, Login, Cadastro e Dados Mockados

## Tema da atividade
Desenvolvimento de um pequeno aplicativo Flutter com navegação entre telas, uso de formulários, validação,
arquitetura organizada e armazenamento temporário de usuários em memória com dados mockados.

Participantes:
João Miguel da Silva Cavalcante 

Gabriel Henrique Sartório RA:25000700

Kayky Kings


# Objetivo da atividade

Desenvolver, em grupo, um aplicativo Flutter seguindo a mesma proposta estrutural vista em aula, contendo:

● **Tela de Splash**

● **Tela de Login**

● **Tela de Cadastro**

● **Tela Home**

# Funcionalidades

Tela de Splash: Primeira tela do aplicativo com transição automática para o Login.


Fluxo de Cadastro: Permite a criação de novos usuários que são armazenados temporariamente em memória.


Autenticação: Validação de credenciais consultando a lista de usuários mockados.


Navegação: Sistema de rotas entre Splash, Login, Cadastro e Home.


Home Page: Tela de destino após um login bem-sucedido.




# Arquitetura e Organização

## O projeto foi estruturado seguindo uma separação clara de responsabilidades:
---
 Models:Definição da entidade UsuarioModel com campos de nome, e-mail e senha.


 Views: Interfaces de usuário utilizando widgets básicos, TextFormField e layouts com Column, Row e Container.


 ViewModels: Lógica de negócio separada da interface para garantir a manutenção do código.


 Data (Mock Store): Gerenciamento de dados em memória utilizando o padrão Singleton.


lib/

 └── app/
 
     ├── data/          # usuario_mock_store.dart (Persistência em memória)
     ├── models/        # usuario_model.dart
     ├── viewmodels/    # Lógica de Splash, Login e Signup
     └── views/         # Interfaces (Splash, Login, Signup, Home)

     
# Persistência em Memória
Para simular um banco de dados sem o uso de APIs externas ou Firebase, foi implementada a classe UsuarioMockStore. Esta classe utiliza uma List<UsuarioModel> interna e fornece métodos para:


Adicionar(UsuarioModel usuario): Insere um novo usuário na lista.


Buscar(String email, String senha): Valida se as credenciais existem para permitir o login.


## Requisitos Técnicos Implementados

Navegação: Utilização de rotas nomeadas para gerenciar a transição entre telas.


Validação de Formulários: Uso de Form e TextFormField com validadores para garantir a integridade das entradas.


Persistência: Dados mantidos em memória durante a execução via List<UsuarioModel>.


Feedback Visual: Implementação de SnackBar para notificar sucesso ao realizar cadastro.

## Comunicação View-ViewModel 

Seguindo o padrão de projet, a interface não processa os dados diretamente:

A View coleta as entradas através de TextEditingController.

A ViewModel valida o estado do formulário via formKey.

Se válido, os dados são enviados para o UsuarioMockStore e a View navega o usuário de volta para a tela de Login.

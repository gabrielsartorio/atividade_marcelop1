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

     

## Requisitos Técnicos Implementados

Navegação: Utilização de rotas nomeadas para gerenciar a transição entre telas.


Validação de Formulários: Uso de Form e TextFormField com validadores para garantir a integridade das entradas.


Persistência: Dados mantidos em memória durante a execução via List<UsuarioModel>.


Feedback Visual: Implementação de SnackBar para notificar sucesso ao realizar cadastro.

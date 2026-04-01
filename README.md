# Projeto Flutter: Fluxo de Autenticação com Dados Mockados

## 1. Descrição do Projeto
Este aplicativo foi desenvolvido como atividade avaliativa para a disciplina de Desenvolvimento de Dispositivos Móveis[cite: 1, 3]. [cite_start]O objetivo é demonstrar a implementação de um fluxo completo de navegação e autenticação, utilizando persistência temporária em memória e uma arquitetura organizada[cite: 4, 11].

O sistema contempla quatro telas principais:
**Splash Screen:** Tela de inicialização com carregamento temporizado[cite: 7, 14].
**Login:** Interface para validação de credenciais[cite: 8, 15].
**Cadastro:** Formulário para registro de novos usuários[cite: 9, 16].
**Home:** Tela de destino após autenticação bem-sucedida[cite: 10, 21].

## 2. Arquitetura Adotada
O projeto utiliza o padrão de separação de responsabilidades (MVVM simplificado) para garantir que a lógica de negócio não resida na camada de interface[cite: 29, 30, 34]:

**Models:** Representação das entidades de dados (`UsuarioModel`)[cite: 63, 64].
**Views:** Implementação da interface do usuário com Widgets nativos do Flutter[cite: 31, 120].
**ViewModels:** Concentração da lógica de validação, navegação e manipulação de dados[cite: 32, 116].
**Data/Store:** Camada de persistência em memória utilizando o padrão Singleton para compartilhamento de dados entre telas[cite: 77, 81, 114].

## 3. Requisitos Técnicos Implementados
Conforme as diretrizes da atividade, foram aplicados os seguintes conceitos:
**Gerenciamento de Dados:** Uso de `List<UsuarioModel>` para armazenamento em memória[cite: 18, 72].
**Navegação:** Implementação de rotas nomeadas para transição entre telas[cite: 97].
**Formulários:** Uso de `TextFormField` com validadores para garantir a integridade dos dados inseridos[cite: 53, 59, 98, 99].
**Layout:** Construção visual baseada em `Container`, `Column` e `Row`, com foco em alinhamento e espaçamento[cite: 39, 42, 43, 44, 45].

## 4. Estrutura de Pastas
lib/
├── app/
│   ├── data/          # Repositório Singleton e lista mockada
│   ├── models/        # Modelos de dados (UsuarioModel)
│   ├── viewmodels/    # Lógica de negócio por tela
│   └── views/         # Arquivos de interface (UI)
└── main.dart          # Configuração de rotas e entrada do app

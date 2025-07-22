# Sistema de Login com Kivy

Este é um projeto de estudo utilizando a biblioteca **Kivy** para criar uma interface gráfica em Python com funcionalidades de **login**, **cadastro de usuários** e **armazenamento local em arquivo `.txt`**.

## Objetivo

Criar uma interface de login simples com suporte a:

- Autenticação de usuários existentes
- Criação de novos usuários com nome, email e senha
- Validação de entradas
- Persistência dos dados em um arquivo local (`users.txt`)

## Estrutura do Projeto

O projeto é dividido em quatro arquivos principais:

ProjetoKivyLoginUsuarios/
├── main.py # Lógica principal da interface Kivy e navegação
├── database.py # Classe para gerenciamento dos usuários
├── my.kv # Definições da interface com Kivy Language
└── users.txt # Arquivo com os dados persistidos dos usuários

## Descrição dos Arquivos

### `database.py`

Este arquivo contém a classe `DataBase`, responsável por:

- Carregar os usuários do `users.txt`
- Adicionar novos usuários
- Validar credenciais
- Salvar alterações
- Retornar informações do usuário
- Registrar a data de criação

### `my.kv`

Define a interface visual com os seguintes componentes:

- `LoginWindow`: tela de login com campos de e-mail e senha
- `CreateAccountWindow`: tela de cadastro com campos de nome, e-mail e senha
- `MainWindow`: tela principal exibida após login com os dados do usuário
- Utiliza `FloatLayout`, `TextInput`, `Label` e `Button` com responsividade baseada no tamanho da janela

### `main.py`

Responsável por:

- Inicializar a aplicação
- Configurar o `ScreenManager`
- Controlar a navegação entre as telas
- Integrar a interface `.kv` com a lógica da aplicação

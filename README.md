# 🚀 Projack Impulse — Central de Projetos

> Plataforma web desenvolvida para centralizar a criação, organização e gerenciamento de projetos, permitindo que usuários acompanhem seus projetos, informações de perfil, colaboradores, tecnologias e repositórios.

## 📌 Sobre o projeto

O **Projack Impulse** é uma plataforma web voltada para a organização e gerenciamento de projetos.

A aplicação permite que usuários criem e visualizem seus projetos, mantenham informações de perfil, adicionem tecnologias e repositórios relacionados aos projetos e gerenciem colaboradores e solicitações de participação.

O sistema possui uma interface com identidade visual própria, inspirada em uma temática espacial, utilizando elementos como foguetes, estrelas e astronautas para representar a ideia de exploração e desenvolvimento de novos projetos.

## ✨ Funcionalidades

### 👤 Usuários

* Cadastro de novos usuários
* Login na plataforma
* Visualização do perfil
* Edição de informações pessoais
* Cadastro de habilidades
* Informações de contato
* Integração de informações do GitHub e LinkedIn

### 📁 Projetos

* Visualização dos projetos do usuário
* Pesquisa de projetos
* Criação de novos projetos
* Visualização individual de um projeto
* Definição do nível de dificuldade
* Definição da categoria
* Acompanhamento do status do projeto
* Edição e exclusão de projetos

### 🧩 Tecnologias e repositórios

Cada projeto pode possuir informações relacionadas a:

* Tecnologias utilizadas
* Repositórios
* Links para repositórios
* Organização dos recursos utilizados no desenvolvimento

### 👥 Colaboradores

A plataforma possui recursos para gerenciamento de colaboradores, incluindo:

* Visualização de colaboradores
* Solicitações de participação
* Aceitação de solicitações
* Organização da equipe do projeto

### 🤖 Seleção de colaboradores com IA

A página individual do projeto possui uma funcionalidade destinada à utilização de inteligência artificial para auxiliar na seleção de colaboradores.

A proposta é utilizar a IA para identificar os candidatos mais adequados para determinado projeto.

## 🛠️ Tecnologias utilizadas

### Front-end

* HTML5
* CSS3
* JavaScript

### Back-end

* Python
* Flask
* Gunicorn

### Integrações

* API externa para autenticação e cadastro
* Google Fonts
* GitHub
* LinkedIn

### Automação

* GitHub Actions

## 🏗️ Estrutura do projeto

```text
Fronts_Projeto-main/
│
├── .github/
│   └── workflows/
│       └── main_fronts.yml
│
├── static/
│   ├── css/
│   │   ├── css_cadastro/
│   │   ├── css_login/
│   │   ├── css_perfil/
│   │   ├── css_projeto_individual/
│   │   └── css_projetos/
│   │
│   ├── imagens/
│   │   ├── imagens_cadastro/
│   │   ├── imagens_login/
│   │   ├── imagens_perfil/
│   │   ├── imagens_projeto_individual/
│   │   └── imagens_projetos/
│   │
│   └── js/
│       ├── js_perfil/
│       └── js_projeto_individual/
│
├── templates/
│   ├── cadastro.html
│   ├── login.html
│   ├── Perfil.html
│   ├── projetos.html
│   └── projeto_individual.html
│
├── app.py
├── requirements.txt
├── .gitignore
└── README.md
```

## 🔄 Fluxo da aplicação

O fluxo principal da plataforma pode ser representado da seguinte forma:

```text
                    ┌──────────────┐
                    │     Login    │
                    └──────┬───────┘
                           │
                           ▼
                    ┌──────────────┐
                    │    Perfil    │
                    └──────┬───────┘
                           │
                           ▼
                    ┌──────────────┐
                    │   Projetos   │
                    └──────┬───────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
       Criar projeto   Pesquisar     Selecionar
                       projetos      projeto
                                         │
                                         ▼
                                ┌─────────────────┐
                                │ Detalhes projeto│
                                └────────┬────────┘
                                         │
                   ┌─────────────────────┼─────────────────────┐
                   ▼                     ▼                     ▼
              Tecnologias          Repositórios          Colaboradores
                                                               │
                                                               ▼
                                                        Solicitações / IA
```

## 🚀 Como executar

### Pré-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

* Python 3
* pip
* Git

### 1. Clone o repositório

```bash
git clone URL_DO_REPOSITORIO
```

Entre na pasta:

```bash
cd Fronts_Projeto-main
```

### 2. Crie um ambiente virtual

Linux/macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Execute a aplicação

```bash
python app.py
```

Caso esteja utilizando Gunicorn para execução em produção:

```bash
gunicorn app:app
```

Depois, acesse a aplicação pelo endereço disponibilizado pelo servidor.

## 🎨 Interface

A aplicação possui uma identidade visual própria, utilizando uma temática espacial para representar a exploração e construção de novos projetos.

Entre os elementos visuais utilizados estão:

* 🚀 Foguetes
* ⭐ Estrelas
* 👨‍🚀 Elementos relacionados ao espaço
* 📁 Cards de projetos
* 👤 Área de perfil
* 🤖 Elementos relacionados à inteligência artificial

## 📱 Páginas

### Login

Página responsável pela autenticação dos usuários.

### Cadastro

Permite o cadastro de novos usuários na plataforma.

### Perfil

Apresenta informações pessoais, contatos e habilidades do usuário.

### Meus Projetos

Área destinada à visualização, pesquisa e criação de projetos.

### Projeto Individual

Apresenta as informações detalhadas de um projeto, incluindo descrição, nível, categoria, status, tecnologias, repositórios, colaboradores e solicitações.

## 🔐 Integração com API

O front-end realiza requisições para uma API externa responsável por operações relacionadas à autenticação e cadastro de usuários.

As requisições são realizadas utilizando `fetch` e comunicação no formato JSON.

> **Observação:** para executar a aplicação completa, pode ser necessário configurar corretamente a API utilizada pelo projeto.

## 🔧 Desenvolvimento

O projeto está estruturado utilizando Flask para servir as páginas HTML e organizar as rotas da aplicação.

A camada visual está separada em:

```text
HTML → Estrutura das páginas
CSS  → Estilização e identidade visual
JS   → Interações e funcionalidades
Flask → Rotas e renderização
```

Essa separação facilita a manutenção e evolução da aplicação.

## 📈 Possíveis melhorias

Algumas melhorias que podem ser implementadas futuramente:

* [ ] Melhorar o gerenciamento de autenticação e sessões
* [ ] Centralizar as configurações da API em variáveis de ambiente
* [ ] Implementar validações mais robustas nos formulários
* [ ] Melhorar o tratamento de erros
* [ ] Integrar completamente o gerenciamento de projetos ao back-end
* [ ] Implementar persistência de dados
* [ ] Expandir a funcionalidade de recomendação de colaboradores por IA
* [ ] Melhorar a responsividade em diferentes dispositivos
* [ ] Automatizar testes
* [ ] Ampliar a documentação da API

## 📚 Contexto acadêmico

O **Projack Impulse** foi desenvolvido como um projeto acadêmico com o objetivo de aplicar conhecimentos de desenvolvimento web, organização de sistemas, interfaces, integração com APIs e gerenciamento de projetos.

## 👨‍💻 Autores

Projeto desenvolvido por estudantes da **Escola de Engenharia da Universidade Presbiteriana Mackenzie**.

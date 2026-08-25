# TechFix

Aplicação web responsiva para cadastro, consulta e gerenciamento de solicitações de manutenção de computadores e notebooks.

## Autor

**Nicolas**

## Sobre o Projeto

O **TechFix** é uma aplicação web desenvolvida para facilitar o contato entre clientes e uma assistência técnica de computadores.

A aplicação permitirá que o usuário consulte os serviços disponíveis, informe dados sobre seu equipamento e registre uma solicitação de manutenção.

O sistema também permitirá consultar as solicitações cadastradas, utilizando uma API fake para persistência dos dados.

O projeto será desenvolvido progressivamente durante a disciplina utilizando HTML5, CSS3, Sass, Bootstrap, JavaScript, jQuery e APIs REST.

## Objetivo

O objetivo principal do TechFix é organizar o processo de solicitação de serviços de assistência técnica, permitindo que o cliente informe previamente:

* Dados pessoais;
* Dados de contato;
* Tipo de equipamento;
* Marca e modelo;
* Serviço desejado;
* Problema apresentado;
* Endereço.

A aplicação deverá possuir uma interface simples, responsiva e de fácil utilização.

## Principais Funcionalidades

* Visualização dos serviços oferecidos;
* Pesquisa e filtragem de serviços;
* Cadastro de solicitações de manutenção;
* Validação de formulários;
* Máscaras para telefone e CEP;
* Consulta automática de endereço;
* Persistência temporária de informações utilizando Web Storage;
* Persistência de solicitações utilizando JSON Server;
* Listagem dinâmica das solicitações cadastradas;
* Exclusão de solicitações;
* Interface responsiva para mobile e desktop.

## Páginas da Aplicação

A aplicação possuirá inicialmente quatro páginas:

### Página Inicial

Apresentação da assistência técnica e dos principais serviços.

### Serviços

Listagem dos serviços de manutenção disponíveis.

### Solicitar Manutenção

Formulário para cadastro de uma nova solicitação.

### Solicitações

Página responsável por apresentar as solicitações cadastradas.

---

## Prototipação

O protótipo da aplicação será inicialmente desenvolvido utilizando o **Google Stitch**, considerando versões para:

* Mobile;
* Desktop.

O protótipo poderá posteriormente ser refinado no Figma.

### Link do Figma

`A definir`

---

## Design System

O Design System da aplicação está documentado no arquivo:

[`docs/architecture.md`](./docs/architecture.md)

Ele contém informações sobre:

* Cores;
* Tipografia;
* Espaçamentos;
* Componentes;
* Responsividade;
* Design Tokens.

---

## Framework CSS

O Framework CSS escolhido para o projeto é:

**Bootstrap 5**

O Bootstrap será utilizado para implementar:

* Sistema de Grid;
* Flexbox;
* Containers;
* Navbar;
* Cards;
* Buttons;
* Forms;
* Alerts;
* Modal;
* Carousel;
* Tabelas;
* Utilitários responsivos.

---

## Dependências

O projeto utilizará:

* Bootstrap 5;
* Bootstrap Icons;
* Sass;
* JavaScript ES6+;
* jQuery;
* jQuery Mask Plugin;
* JSON Server;
* ESLint;
* Prettier.

---

## API Pública

A aplicação utilizará a API pública:

**ViaCEP**

A ViaCEP será utilizada para consultar automaticamente dados de endereço através do CEP informado pelo cliente.

Entre as informações retornadas estarão:

* Logradouro;
* Bairro;
* Cidade;
* Estado.

---

## API Fake

Será utilizado o **JSON Server** para simular uma API REST.

A API será responsável principalmente pelos recursos:

```text
/services
/requests
```

Esses endpoints serão utilizados para armazenar e consultar:

* Serviços;
* Solicitações de manutenção.

---

# Checklist de Indicadores de Desempenho

## RA1 — Frameworks CSS e Responsividade

* [ ] **ID 01** — Prototipar interfaces adaptáveis para mobile e desktop utilizando Stitch/Figma.
* [ ] **ID 02** — Implementar layout responsivo utilizando Grid ou Flexbox do Bootstrap.
* [ ] **ID 03** — Implementar partes do layout utilizando Flexbox ou Grid com CSS puro.
* [ ] **ID 04** — Utilizar componentes prontos do Bootstrap e componentes JavaScript do framework.
* [ ] **ID 05** — Criar layout fluido utilizando unidades relativas como %, rem, em, vw e vh.
* [ ] **ID 06** — Aplicar Design System consistente em toda a aplicação.
* [ ] **ID 07** — Utilizar Sass com variáveis, mixins e funções.
* [ ] **ID 08** — Aplicar tipografia responsiva utilizando `clamp()` ou media queries.
* [ ] **ID 09** — Aplicar técnicas de responsividade de imagens utilizando CSS.
* [ ] **ID 10** — Utilizar imagens otimizadas em WebP e recursos como `srcset` ou `picture`.

## RA2 — Formulários e Validação

* [ ] **ID 11** — Implementar validação HTML nativa.
* [ ] **ID 12** — Utilizar expressões regulares para validações customizadas.
* [ ] **ID 13** — Utilizar elementos `select`, `radio` e `checkbox`.
* [ ] **ID 14** — Utilizar LocalStorage ou SessionStorage.

## RA3 — Ferramentas de Desenvolvimento

* [ ] **ID 15** — Configurar Node.js e NPM.
* [ ] **ID 16** — Utilizar boas práticas de versionamento com Git e GitHub.
* [ ] **ID 17** — Manter README padronizado.
* [ ] **ID 18** — Organizar os arquivos da aplicação de maneira modular.
* [ ] **ID 19** — Configurar ESLint e Prettier.

## RA4 — Bibliotecas JavaScript

* [ ] **ID 20** — Utilizar jQuery para manipulação do DOM e interatividade.
* [ ] **ID 21** — Integrar o jQuery Mask Plugin.

## RA5 — APIs

* [ ] **ID 22** — Utilizar requisições assíncronas para cadastrar dados no JSON Server.
* [ ] **ID 23** — Utilizar requisições assíncronas para consultar dados do JSON Server.
* [ ] **ID 24** — Consumir a API pública ViaCEP utilizando requisições assíncronas.

---

## Estrutura Planejada

```text
techfix/
│
├── index.html
├── servicos.html
├── solicitar.html
├── solicitacoes.html
│
├── assets/
│   ├── icons/
│   └── images/
│
├── css/
│   └── style.css
│
├── scss/
│   ├── _variables.scss
│   ├── _mixins.scss
│   ├── _components.scss
│   └── style.scss
│
├── js/
│   ├── main.js
│   ├── services.js
│   ├── request-form.js
│   └── requests.js
│
├── docs/
│   ├── prd.md
│   └── architecture.md
│
├── db.json
├── package.json
├── .gitignore
├── .eslintrc
├── .prettierrc
└── README.md
```

---

## Site em Produção

O projeto será publicado utilizando **GitHub Pages**.

Link:

`A definir`

---

## Execução Local

### 1. Clonar o projeto

```bash
git clone URL-DO-REPOSITORIO
```

### 2. Entrar na pasta

```bash
cd techfix
```

### 3. Instalar as dependências

```bash
npm install
```

### 4. Executar o JSON Server

```bash
npm run server
```

### 5. Compilar o Sass

```bash
npm run sass
```

### 6. Executar a aplicação

A aplicação poderá ser aberta utilizando um servidor local, como a extensão Live Server do Visual Studio Code.

---

## Telas da Aplicação

As imagens serão adicionadas durante o desenvolvimento.

### Home

`Imagem a adicionar`

### Serviços

`Imagem a adicionar`

### Solicitar Manutenção

`Imagem a adicionar`

### Solicitações

`Imagem a adicionar`

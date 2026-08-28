# TechFix

Aplicação web responsiva para consulta de serviços e cadastro de solicitações de manutenção de computadores e notebooks.

## Autor

**Nicolas**

## Descrição do Projeto

O **TechFix** é uma aplicação web criada para facilitar o processo de solicitação de serviços de manutenção de computadores e notebooks.

A aplicação permitirá que o usuário consulte os serviços oferecidos por uma assistência técnica, pesquise e filtre serviços e registre uma solicitação de atendimento informando seus dados pessoais, endereço, equipamento e problema apresentado.

Os dados das solicitações serão armazenados em uma API fake utilizando **JSON Server** e posteriormente exibidos dinamicamente na aplicação.

Além disso, o sistema consumirá a API pública **ViaCEP** para consultar automaticamente informações de endereço a partir do CEP informado pelo usuário.

O projeto será desenvolvido progressivamente utilizando tecnologias frontend e seguirá uma abordagem responsiva para dispositivos mobile e desktop.

---

## Objetivo

O objetivo do TechFix é oferecer uma forma simples e organizada para que clientes possam consultar serviços de assistência técnica e registrar solicitações de manutenção.

A aplicação também será utilizada como projeto prático para aplicação dos conteúdos estudados durante a disciplina, incluindo:

* HTML5;
* CSS3;
* Bootstrap;
* Sass;
* JavaScript ES6+;
* jQuery;
* Web Storage;
* JSON Server;
* Consumo de APIs;
* Responsividade;
* Git e GitHub.

---

## Páginas da Aplicação

O projeto possuirá inicialmente quatro páginas:

### Home

Página inicial responsável por apresentar o TechFix, seus principais serviços e informações gerais.

### Serviços

Página responsável por listar os serviços de manutenção disponíveis.

Permitirá pesquisar e filtrar os serviços.

### Solicitar Manutenção

Página contendo o formulário utilizado para cadastrar uma nova solicitação.

### Solicitações

Página responsável por apresentar as solicitações registradas no sistema.

---

## Prototipação

O protótipo será desenvolvido inicialmente no **Google Stitch**, contemplando versões para:

* Mobile;
* Desktop.

O protótipo poderá posteriormente ser refinado no Figma.

### Link do Figma

`A definir`

---

## Design System

O Design System completo da aplicação está documentado em:

[`docs/architecture.md`](./docs/architecture.md)

O documento apresenta:

* Paleta de cores;
* Tipografia;
* Espaçamentos;
* Bordas;
* Responsividade;
* Componentes;
* Design Tokens.

---

## Framework CSS

O Framework CSS escolhido para o projeto é:

**Bootstrap 5**

O Bootstrap será utilizado para:

* Grid responsivo;
* Flexbox;
* Containers;
* Navbar;
* Cards;
* Buttons;
* Forms;
* Alerts;
* Modal;
* Tabelas;
* Badges;
* Utilitários responsivos.

Os principais componentes planejados no protótipo que posteriormente serão implementados com Bootstrap são:

1. Navbar;
2. Cards de serviços;
3. Modal de detalhes e confirmação.

---

## Dependências

O projeto utilizará:

* Bootstrap 5;
* Bootstrap Icons;
* JavaScript ES6+;
* Sass;
* jQuery;
* jQuery Mask Plugin;
* JSON Server;
* ESLint;
* Prettier.

---

## API Pública

A API pública escolhida para o projeto é a **ViaCEP**.

Ela será utilizada no formulário de solicitação para consultar automaticamente informações de endereço a partir do CEP informado pelo cliente.

Entre os dados utilizados estarão:

* Logradouro;
* Bairro;
* Cidade;
* Estado.

---

## API Fake

Será utilizado o **JSON Server** para simular uma API REST.

Os principais recursos da API serão:

```text
/services
/requests
```

### `/services`

Responsável por armazenar e fornecer os serviços disponíveis.

### `/requests`

Responsável por armazenar e fornecer as solicitações de manutenção.

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

# Checklist de Indicadores de Desempenho

## RA1 — Framework CSS e Responsividade

* [ ] **ID 01** — Prototipar interfaces adaptáveis para mobile e desktop utilizando Stitch ou Figma.
* [ ] **ID 02** — Implementar layout responsivo utilizando Grid ou Flexbox do Bootstrap.
* [ ] **ID 03** — Implementar partes do layout utilizando Flexbox ou Grid com CSS puro.
* [ ] **ID 04** — Utilizar componentes prontos do Bootstrap e componentes JavaScript do framework.
* [ ] **ID 05** — Utilizar unidades relativas como `rem`, `em`, `%`, `vw` e `vh`.
* [ ] **ID 06** — Aplicar um Design System consistente em toda a aplicação.
* [ ] **ID 07** — Utilizar Sass com variáveis, mixins e funções.
* [ ] **ID 08** — Aplicar tipografia responsiva utilizando media queries ou `clamp()`.
* [ ] **ID 09** — Aplicar técnicas de responsividade de imagens utilizando CSS.
* [ ] **ID 10** — Utilizar imagens WebP e carregamento adaptativo com `srcset` ou `picture`.

## RA2 — Formulários e Validação

* [ ] **ID 11** — Implementar validação HTML nativa com campos obrigatórios e mensagens de erro ou sucesso.
* [ ] **ID 12** — Aplicar expressões regulares para validações customizadas.
* [ ] **ID 13** — Utilizar elementos `checkbox`, `radio` e `select`.
* [ ] **ID 14** — Utilizar LocalStorage ou SessionStorage para persistência local.

## RA3 — Ferramentas de Desenvolvimento

* [ ] **ID 15** — Configurar Node.js e NPM.
* [ ] **ID 16** — Utilizar boas práticas de versionamento com Git e GitHub.
* [ ] **ID 17** — Manter o README padronizado e atualizado.
* [ ] **ID 18** — Organizar os arquivos do projeto de forma modular.
* [ ] **ID 19** — Configurar ESLint e Prettier.

## RA4 — Bibliotecas JavaScript

* [ ] **ID 20** — Utilizar jQuery para manipulação do DOM e interatividade.
* [ ] **ID 21** — Utilizar o jQuery Mask Plugin ou biblioteca equivalente.

## RA5 — APIs

* [ ] **ID 22** — Realizar requisições assíncronas para persistir dados no JSON Server.
* [ ] **ID 23** — Realizar requisições assíncronas para consultar dados do JSON Server.
* [ ] **ID 24** — Consumir a API pública ViaCEP e tratar possíveis erros.

---

## Instruções de Execução

### 1. Clonar o repositório

```bash
git clone https://github.com/lolo-irl/techfix.git
```

### 2. Entrar no projeto

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

### 6. Executar o projeto

Abrir a aplicação utilizando um servidor local, como o **Live Server** do Visual Studio Code.

---

## Site em Produção

O frontend será publicado utilizando **GitHub Pages**.

**Link:** `A definir`

---

## Telas da Aplicação

As imagens serão adicionadas após a criação do protótipo e implementação das páginas.

### Home

`Imagem a adicionar`

### Serviços

`Imagem a adicionar`

### Solicitar Manutenção

`Imagem a adicionar`

### Solicitações

`Imagem a adicionar`


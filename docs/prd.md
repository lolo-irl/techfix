# Product Requirements Document — TechFix

## 1. Identificação

**Projeto:** TechFix
**Tema:** Sistema Web para Solicitação de Manutenção de Computadores
**Autor:** Nicolas Costa Boese

---

# 2. Visão Geral

O **TechFix** é uma aplicação web responsiva destinada à consulta de serviços e ao cadastro de solicitações de manutenção de computadores e notebooks.

O sistema permitirá que pessoas interessadas em serviços de assistência técnica consultem os serviços disponíveis e registrem uma solicitação informando seus dados pessoais, endereço, equipamento e problema apresentado.

O projeto será desenvolvido progressivamente ao longo da disciplina, aplicando os conteúdos estudados em HTML, CSS, Framework CSS, Sass, JavaScript, bibliotecas JavaScript, Web Storage e consumo de APIs.

---

# 3. Problema

Solicitações de manutenção realizadas apenas por telefone ou aplicativos de mensagens podem gerar informações incompletas e dificultar a organização dos atendimentos.

O cliente pode deixar de informar dados importantes como:

* Tipo do equipamento;
* Marca;
* Modelo;
* Serviço desejado;
* Problema apresentado;
* Telefone;
* E-mail;
* Endereço.

Isso pode exigir várias mensagens adicionais entre a assistência e o cliente antes mesmo do início do atendimento.

---

# 4. Solução Proposta

O TechFix oferecerá uma interface web estruturada na qual o usuário poderá:

1. Conhecer a assistência técnica;
2. Consultar os serviços disponíveis;
3. Pesquisar e filtrar serviços;
4. Visualizar informações detalhadas de um serviço;
5. Preencher uma solicitação de manutenção;
6. Consultar automaticamente seu endereço pelo CEP;
7. Validar os dados informados;
8. Enviar a solicitação;
9. Consultar as solicitações cadastradas.

---

# 5. Objetivo Geral

Desenvolver uma aplicação web responsiva que facilite o registro e a consulta de solicitações de manutenção de computadores.

---

# 6. Objetivos Específicos

O projeto deverá:

* Possuir pelo menos três páginas HTML distintas;
* Funcionar corretamente em mobile e desktop;
* Utilizar Bootstrap como Framework CSS;
* Possuir componentes responsivos;
* Utilizar um Design System consistente;
* Possuir formulário com validação;
* Utilizar Web Storage;
* Manipular dinamicamente o DOM;
* Utilizar jQuery;
* Consumir uma API fake;
* Consumir uma API pública;
* Apresentar dados de forma dinâmica.

---

# 7. Público-Alvo

O público-alvo do TechFix são pessoas que possuem computadores ou notebooks e desejam contratar algum serviço relacionado a:

* Manutenção;
* Limpeza;
* Formatação;
* Diagnóstico;
* Upgrade;
* Instalação de programas;
* Correção de problemas de hardware ou software.

---

# 8. Atores do Sistema

## 8.1 Visitante

Pessoa que acessa a aplicação para conhecer os serviços disponíveis.

O visitante poderá:

* Visualizar a página inicial;
* Navegar pelo sistema;
* Consultar os serviços;
* Pesquisar serviços;
* Filtrar serviços;
* Visualizar detalhes de um serviço.

---

## 8.2 Cliente

Pessoa que deseja registrar uma solicitação de manutenção.

O cliente poderá:

* Informar seus dados pessoais;
* Informar telefone e e-mail;
* Informar o CEP;
* Consultar automaticamente o endereço;
* Informar os dados do equipamento;
* Selecionar o serviço desejado;
* Descrever o problema;
* Escolher sua preferência de contato;
* Enviar uma solicitação;
* Consultar solicitações cadastradas.

Nesta versão do projeto não será necessária autenticação de usuários.

---

# 9. Escopo Funcional

A aplicação será composta inicialmente por quatro páginas.

## 9.1 Home

A página inicial deverá apresentar:

* Navbar;
* Seção principal de apresentação;
* Descrição do TechFix;
* Serviços em destaque;
* Benefícios da assistência;
* Chamada para solicitar atendimento;
* Footer.

---

## 9.2 Serviços

A página apresentará os serviços de manutenção disponíveis.

Cada serviço deverá conter:

* Nome;
* Categoria;
* Descrição;
* Imagem;
* Preço estimado, quando aplicável.

A página poderá disponibilizar:

* Pesquisa por nome;
* Filtro por categoria;
* Modal com detalhes;
* Botão para iniciar uma solicitação.

---

## 9.3 Solicitar Manutenção

A página será responsável pelo cadastro de uma nova solicitação.

O formulário deverá conter:

### Dados do cliente

* Nome;
* E-mail;
* Telefone.

### Endereço

* CEP;
* Logradouro;
* Bairro;
* Cidade;
* Estado.

### Equipamento

* Tipo;
* Marca;
* Modelo.

### Atendimento

* Serviço desejado;
* Preferência de contato;
* Descrição do problema;
* Confirmação dos dados.

---

## 9.4 Solicitações

A página deverá apresentar dinamicamente as solicitações cadastradas.

Cada solicitação poderá apresentar:

* Nome do cliente;
* Serviço;
* Equipamento;
* Marca;
* Modelo;
* Descrição do problema;
* Data;
* Status.

A listagem poderá utilizar cards ou tabela.

---

# 10. Histórias de Usuário

## US01 — Visualizar a aplicação

**Como visitante, quero visualizar uma página inicial responsiva para entender rapidamente o objetivo do TechFix em qualquer dispositivo.**

### Critérios de aceitação

* A página deve possuir versão mobile e desktop;
* O conteúdo deve permanecer legível em diferentes tamanhos de tela;
* Deve possuir navegação para as principais páginas.

---

## US02 — Navegar entre páginas

**Como visitante, quero utilizar uma barra de navegação para acessar facilmente as diferentes páginas da aplicação.**

### Critérios de aceitação

* A Navbar deverá aparecer nas páginas principais;
* Em telas menores, a navegação deverá se adaptar ao formato mobile.

---

## US03 — Visualizar serviços

**Como visitante, quero consultar os serviços disponíveis para identificar qual opção atende ao problema do meu equipamento.**

### Critérios de aceitação

Cada serviço deve apresentar:

* Nome;
* Categoria;
* Descrição;
* Imagem.

---

## US04 — Pesquisar serviços

**Como visitante, quero pesquisar um serviço pelo nome para encontrar rapidamente o atendimento desejado.**

### Critérios de aceitação

* A listagem deverá ser atualizada de acordo com o texto digitado;
* A interação poderá utilizar jQuery.

---

## US05 — Filtrar serviços

**Como visitante, quero filtrar os serviços por categoria para visualizar apenas opções relacionadas à minha necessidade.**

Categorias possíveis:

* Hardware;
* Software;
* Limpeza;
* Upgrade;
* Diagnóstico.

---

## US06 — Visualizar detalhes

**Como visitante, quero visualizar mais informações sobre um serviço antes de fazer uma solicitação.**

### Critérios de aceitação

Os detalhes poderão ser exibidos utilizando um Modal do Bootstrap.

---

## US07 — Preencher uma solicitação

**Como cliente, quero preencher um formulário para registrar uma solicitação de manutenção.**

### Critérios de aceitação

O formulário deverá:

* Possuir campos obrigatórios;
* Utilizar validação HTML;
* Utilizar validações JavaScript quando necessário;
* Exibir mensagens de erro;
* Exibir mensagem de sucesso.

---

## US08 — Validar informações

**Como cliente, quero ser informado quando um dado estiver inválido para poder corrigi-lo antes de enviar a solicitação.**

### Critérios de aceitação

Serão utilizados:

* `required`;
* `type`;
* `minlength`;
* `maxlength`;
* Expressões regulares;
* Mensagens visuais de validação.

---

## US09 — Formatar telefone

**Como cliente, quero que meu telefone seja formatado automaticamente durante o preenchimento para facilitar a digitação e evitar erros.**

Formato esperado:

```text
(42) 99999-9999
```

A funcionalidade utilizará o jQuery Mask Plugin.

---

## US10 — Consultar endereço pelo CEP

**Como cliente, quero informar meu CEP e receber automaticamente os dados do meu endereço para reduzir o preenchimento manual.**

### Critérios de aceitação

* O CEP deverá ser validado;
* A aplicação deverá consultar a ViaCEP;
* Os campos de endereço deverão ser preenchidos quando possível;
* Erros deverão ser informados ao usuário.

---

## US11 — Salvar formulário temporariamente

**Como cliente, quero que parte das informações digitadas seja armazenada temporariamente para evitar perder meu preenchimento caso a página seja recarregada.**

A funcionalidade utilizará LocalStorage ou SessionStorage.

---

## US12 — Selecionar serviço

**Como cliente, quero escolher o serviço desejado para indicar à assistência qual atendimento preciso.**

Será utilizado um elemento `select`.

---

## US13 — Escolher preferência de contato

**Como cliente, quero escolher minha forma preferida de contato para facilitar a comunicação com a assistência.**

Opções possíveis:

* WhatsApp;
* Telefone;
* E-mail.

Serão utilizados elementos `radio`.

---

## US14 — Confirmar envio dos dados

**Como cliente, quero confirmar que revisei as informações fornecidas antes de enviar minha solicitação.**

Será utilizado um `checkbox`.

---

## US15 — Enviar solicitação

**Como cliente, quero enviar minha solicitação para que ela seja registrada no sistema.**

### Critérios de aceitação

* Os dados deverão ser enviados ao JSON Server;
* A requisição deverá ser assíncrona;
* A aplicação deverá tratar erros;
* O usuário deverá receber feedback da operação.

---

## US16 — Consultar solicitações

**Como usuário, quero visualizar as solicitações cadastradas para consultar os atendimentos registrados.**

### Critérios de aceitação

* Os dados deverão ser carregados do JSON Server;
* A requisição deverá ser assíncrona;
* Os elementos deverão ser gerados dinamicamente no DOM.

---

## US17 — Excluir solicitação

**Como usuário, quero excluir uma solicitação cadastrada incorretamente para manter a listagem organizada.**

Essa funcionalidade é complementar ao escopo mínimo.

---

# 11. Regras de Negócio

## RN01 — Campos obrigatórios

Uma solicitação somente poderá ser enviada quando todos os campos definidos como obrigatórios estiverem preenchidos corretamente.
A primeira versão funcional do projeto deverá permitir que o usuário:

1. Acesse a aplicação;
2. Navegue pelas páginas;
3. Consulte serviços;
4. Pesquise ou filtre serviços;
5. Preencha uma solicitação;
6. Receba validações de formulário;
7. Consulte um CEP;
8. Envie uma solicitação;
9. Consulte as solicitações cadastradas.

---

# 14. Fora do Escopo

Nesta versão não serão obrigatórios:

* Login;
* Cadastro de conta;
* Autenticação;
* Recuperação de senha;
* Pagamentos;
* Chat;
* Backend próprio;
* Banco de dados SQL;
* Sistema de permissões;
* Painel administrativo completo.

Essas funcionalidades poderão ser consideradas futuramente.
## RN02 — Nome

O cliente deverá informar um nome válido.

## RN03 — E-mail

O e-mail deverá possuir formato válido.

## RN04 — Telefone

O telefone deverá seguir o formato brasileiro utilizado pela aplicação.

Exemplo:

```text
(42) 99999-9999
```

## RN05 — CEP

O CEP deverá possuir oito dígitos.

Exemplo:

```text
85000-000
```

## RN06 — Consulta do CEP

Quando um CEP válido for informado, a aplicação deverá tentar consultar a API ViaCEP.

## RN07 — Erro na consulta

Se a consulta do CEP não puder ser realizada, o sistema deverá informar o problema ao usuário e permitir o preenchimento manual do endereço.

## RN08 — Serviço

Toda solicitação deverá estar associada a um serviço disponível.

## RN09 — Equipamento

Toda solicitação deverá informar pelo menos o tipo e a marca do equipamento.

## RN10 — Descrição

Toda solicitação deverá possuir uma descrição do problema respeitando os limites definidos pelo formulário.

## RN11 — Status inicial

Toda nova solicitação deverá ser criada com o status:

```text
Pendente
```

## RN12 — Confirmação

O cliente deverá confirmar os dados antes do envio da solicitação.

---

# 12. Requisitos Não Funcionais

## RNF01 — Responsividade

Todas as páginas deverão funcionar adequadamente em telas mobile e desktop.

## RNF02 — Design consistente

A aplicação deverá seguir o mesmo Design System em todas as páginas.

## RNF03 — Usabilidade

A navegação e as ações principais deverão possuir identificação clara.

## RNF04 — Feedback

A aplicação deverá informar ao usuário o resultado das principais operações.

## RNF05 — Organização

HTML, Sass/CSS e JavaScript deverão ser organizados em arquivos de acordo com suas responsabilidades.

## RNF06 — Compatibilidade

A aplicação deverá funcionar em navegadores modernos.

## RNF07 — Manutenção

O Sass deverá ser utilizado para melhorar a modularização e manutenção dos estilos.

---

# 13. Critérios de Sucesso

O projeto será considerado funcional quando for possível:

1. Acessar a aplicação em mobile e desktop;
2. Navegar entre as páginas;
3. Visualizar os serviços;
4. Pesquisar ou filtrar serviços;
5. Preencher o formulário;
6. Receber validações para dados inválidos;
7. Consultar um CEP;
8. Enviar uma solicitação ao JSON Server;
9. Visualizar a solicitação cadastrada.

---

# 14. Fora do Escopo

Para manter o projeto compatível com o tempo e os objetivos da disciplina, não serão obrigatórios nesta versão:

* Login;
* Cadastro de contas;
* Autenticação;
* Recuperação de senha;
* Pagamentos;
* Chat;
* Backend próprio;
* Banco de dados SQL;
* Sistema de permissões;
* Painel administrativo completo.


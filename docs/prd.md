# Product Requirements Document — TechFix

## 1. Identificação

**Projeto:** TechFix
**Tema:** Sistema de Solicitação e Gerenciamento de Manutenção de Computadores
**Autor:** Nicolas

---

# 2. Visão do Produto

O **TechFix** é uma aplicação web responsiva destinada a facilitar o processo de solicitação de manutenção de computadores e notebooks.

A aplicação permitirá que visitantes conheçam os serviços oferecidos pela assistência técnica e que clientes registrem solicitações informando seus dados pessoais, informações sobre o equipamento e uma descrição do problema apresentado.

O projeto busca aplicar os conhecimentos desenvolvidos durante a disciplina de forma progressiva, utilizando tecnologias de desenvolvimento web frontend, bibliotecas JavaScript, Framework CSS, Web Storage e integração com APIs.

---

# 3. Problema

Solicitações de manutenção realizadas exclusivamente por telefone ou aplicativos de mensagens podem gerar dificuldades na organização dos atendimentos.

Frequentemente informações importantes deixam de ser fornecidas pelo cliente, como:

* Tipo de equipamento;
* Marca;
* Modelo;
* Defeito apresentado;
* Serviço desejado;
* Dados de contato;
* Endereço.

Isso pode resultar em várias mensagens adicionais entre cliente e assistência técnica antes mesmo do início do atendimento.

O TechFix busca centralizar essas informações através de um formulário estruturado.

---

# 4. Solução

O TechFix fornecerá uma interface na qual o cliente poderá:

1. Consultar os serviços disponíveis;
2. Encontrar informações sobre cada serviço;
3. Registrar seus dados;
4. Informar os dados do equipamento;
5. Descrever o problema apresentado;
6. Selecionar o serviço desejado;
7. Consultar automaticamente seu endereço utilizando o CEP;
8. Enviar uma solicitação de manutenção;
9. Consultar posteriormente as solicitações cadastradas.

---

# 5. Objetivo Geral

Desenvolver uma aplicação web responsiva para gerenciamento de solicitações de manutenção de computadores, aplicando corretamente as tecnologias e conceitos trabalhados durante a disciplina.

---

# 6. Objetivos Específicos

A aplicação deverá:

* Possuir interface responsiva;
* Utilizar Framework CSS;
* Utilizar CSS personalizado;
* Implementar Design System consistente;
* Utilizar Sass;
* Possuir formulários validados;
* Utilizar Web Storage;
* Manipular elementos do DOM;
* Utilizar jQuery;
* Consumir uma API pública;
* Consumir uma API fake;
* Renderizar dados dinamicamente.

---

# 7. Público-Alvo

O público-alvo do TechFix são pessoas que possuem computadores ou notebooks e precisam contratar serviços de:

* Manutenção;
* Limpeza;
* Formatação;
* Instalação de software;
* Upgrade;
* Diagnóstico;
* Reparos básicos.

O sistema é voltado principalmente para usuários que desejam realizar uma solicitação de forma rápida e organizada.

---

# 8. Atores

## 8.1 Visitante

Pessoa que acessa a aplicação sem necessariamente cadastrar uma solicitação.

O visitante poderá:

* Visualizar a página inicial;
* Conhecer a assistência;
* Navegar entre as páginas;
* Consultar serviços;
* Pesquisar serviços;
* Visualizar detalhes dos serviços.

---

## 8.2 Cliente

Usuário que deseja solicitar um serviço de manutenção.

O cliente poderá:

* Preencher seus dados;
* Informar seu telefone;
* Informar seu endereço;
* Consultar endereço pelo CEP;
* Informar os dados do equipamento;
* Selecionar um serviço;
* Descrever o problema;
* Enviar uma solicitação;
* Consultar solicitações cadastradas.

Não será necessária autenticação nesta versão do projeto.

---

# 9. Escopo

A aplicação possuirá inicialmente quatro páginas principais.

---

## 9.1 Página Inicial

A página inicial será responsável pela apresentação da aplicação.

Deverá apresentar:

* Navbar;
* Hero;
* Descrição do TechFix;
* Serviços em destaque;
* Benefícios da assistência;
* Chamada para solicitar manutenção;
* Rodapé.

---

## 9.2 Página de Serviços

A página de serviços apresentará os serviços disponíveis.

Cada serviço poderá conter:

* Nome;
* Categoria;
* Descrição;
* Imagem;
* Preço estimado;
* Botão de detalhes;
* Botão para solicitar atendimento.

Também será possível implementar:

* Pesquisa;
* Filtro por categoria.

---

## 9.3 Página de Solicitação

A página conterá o formulário principal da aplicação.

O formulário poderá conter:

### Dados pessoais

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
* Categoria do problema;
* Preferência de contato;
* Descrição do problema.

Também serão utilizados campos do tipo:

* `select`;
* `radio`;
* `checkbox`.

---

## 9.4 Página de Solicitações

A página apresentará dinamicamente as solicitações cadastradas.

Cada solicitação poderá apresentar:

* Cliente;
* Serviço;
* Equipamento;
* Problema;
* Data;
* Status.

As informações serão carregadas através de requisições assíncronas ao JSON Server.

---

# 10. Histórias de Usuário

## US01 — Visualizar a página inicial

**Como visitante, quero visualizar uma página inicial clara e responsiva para compreender rapidamente o objetivo do TechFix.**

### Critérios de aceitação

* A página deve funcionar em mobile e desktop;
* Deve possuir identidade visual consistente;
* Deve apresentar navegação para as demais páginas.

---

## US02 — Navegar pela aplicação

**Como visitante, quero utilizar uma barra de navegação para acessar facilmente as diferentes áreas da aplicação.**

### Critérios de aceitação

* A Navbar deve estar disponível nas páginas principais;
* Em dispositivos pequenos, a navegação deve ser adaptada para mobile.

---

## US03 — Visualizar serviços

**Como visitante, quero visualizar os serviços oferecidos para identificar qual manutenção atende às minhas necessidades.**

### Critérios de aceitação

Cada serviço deverá apresentar pelo menos:

* Nome;
* Categoria;
* Descrição;
* Imagem.

---

## US04 — Pesquisar serviços

**Como visitante, quero pesquisar serviços pelo nome para encontrar rapidamente uma opção específica.**

### Critérios de aceitação

* A pesquisa deverá atualizar os resultados apresentados;
* A manipulação poderá ser realizada com jQuery.

---

## US05 — Filtrar serviços

**Como visitante, quero filtrar os serviços por categoria para visualizar apenas as opções relevantes.**

### Categorias possíveis

* Hardware;
* Software;
* Limpeza;
* Upgrade;
* Diagnóstico.

---

## US06 — Visualizar detalhes de um serviço

**Como visitante, quero visualizar informações detalhadas sobre um serviço antes de realizar uma solicitação.**

Os detalhes poderão ser apresentados utilizando um **Modal do Bootstrap**.

---

## US07 — Cadastrar uma solicitação

**Como cliente, quero preencher um formulário para registrar uma solicitação de manutenção.**

### Critérios de aceitação

O formulário deverá possuir:

* Campos obrigatórios;
* Validação HTML;
* Validação JavaScript;
* Feedback de erro;
* Feedback de sucesso.

---

## US08 — Validar meus dados

**Como cliente, quero ser avisado caso alguma informação esteja inválida para poder corrigir os dados antes de enviar a solicitação.**

Serão utilizadas:

* Validações HTML nativas;
* Expressões regulares;
* JavaScript.

---

## US09 — Formatar telefone

**Como cliente, quero que meu telefone seja formatado automaticamente durante a digitação para facilitar o preenchimento.**

Será utilizado o **jQuery Mask Plugin**.

Exemplo:

```text
(42) 99999-9999
```

---

## US10 — Consultar endereço

**Como cliente, quero informar meu CEP e ter meu endereço preenchido automaticamente para reduzir o preenchimento manual.**

A funcionalidade utilizará a API **ViaCEP**.

---

## US11 — Armazenar formulário temporariamente

**Como cliente, quero que parte das informações preenchidas seja salva temporariamente para evitar perder meus dados ao atualizar a página.**

A funcionalidade utilizará:

```text
localStorage
```

---

## US12 — Escolher serviço

**Como cliente, quero selecionar o serviço desejado para informar à assistência qual manutenção preciso realizar.**

Será utilizado um elemento:

```html
<select>
```

---

## US13 — Escolher preferência de contato

**Como cliente, quero informar minha forma preferida de contato para facilitar a comunicação com a assistência.**

Possíveis opções:

* WhatsApp;
* Telefone;
* E-mail.

Poderão ser utilizados elementos `radio`.

---

## US14 — Confirmar informações

**Como cliente, quero confirmar que os dados informados estão corretos antes de enviar minha solicitação.**

Será utilizado um `checkbox`.

---

## US15 — Enviar solicitação

**Como cliente, quero enviar a solicitação para que seus dados sejam registrados no sistema.**

Os dados serão enviados ao JSON Server utilizando uma requisição:

```text
POST /requests
```

---

## US16 — Receber confirmação

**Como cliente, quero receber uma mensagem de sucesso quando minha solicitação for cadastrada para ter certeza de que o processo foi concluído.**

A mensagem poderá ser apresentada através de:

* Bootstrap Alert;
* Modal.

---

## US17 — Consultar solicitações

**Como usuário, quero visualizar as solicitações cadastradas para consultar os atendimentos registrados.**

Os dados serão obtidos utilizando:

```text
GET /requests
```

---

## US18 — Excluir uma solicitação

**Como usuário, quero excluir uma solicitação cadastrada incorretamente para manter a listagem organizada.**

A operação utilizará:

```text
DELETE /requests/:id
```

---

# 11. Regras de Negócio

## RN01 — Campos obrigatórios

Uma solicitação somente poderá ser enviada caso todos os campos obrigatórios estejam corretamente preenchidos.

---

## RN02 — Nome

O cliente deverá informar um nome válido.

---

## RN03 — E-mail

O e-mail deverá possuir formato válido.

Exemplo:

```text
usuario@email.com
```

---

## RN04 — Telefone

O telefone deverá possuir formato brasileiro válido.

Exemplo:

```text
(42) 99999-9999
```

---

## RN05 — CEP

O CEP deverá possuir oito números.

Exemplo:

```text
85000-000
```

---

## RN06 — Consulta de endereço

Ao informar um CEP válido, a aplicação deverá tentar consultar a API ViaCEP.

---

## RN07 — Falha da API

Caso a ViaCEP não possa retornar os dados, a aplicação deverá informar o erro ao usuário.

O preenchimento manual do endereço continuará disponível.

---

## RN08 — Serviço obrigatório

Cada solicitação deverá estar associada a um serviço.

---

## RN09 — Equipamento obrigatório

Cada solicitação deverá possuir um tipo de equipamento.

---

## RN10 — Descrição do problema

O cliente deverá fornecer uma descrição do problema dentro dos limites definidos pelo formulário.

---

## RN11 — Status inicial

Toda nova solicitação será cadastrada inicialmente com o status:

```text
Pendente
```

---

## RN12 — Confirmação

O cliente deverá confirmar o envio dos dados antes da criação da solicitação.

---

# 12. Requisitos Não Funcionais

## RNF01 — Responsividade

Todas as páginas deverão funcionar adequadamente em dispositivos mobile e desktop.

---

## RNF02 — Consistência visual

Todas as páginas deverão utilizar o mesmo Design System.

---

## RNF03 — Usabilidade

Os elementos de navegação e interação deverão possuir identificação clara.

---

## RNF04 — Feedback

A aplicação deverá exibir feedback visual após ações importantes.

---

## RNF05 — Compatibilidade

O sistema deverá funcionar nos principais navegadores modernos.

---

## RNF06 — Organização

O código deverá ser separado em arquivos e diretórios de acordo com sua responsabilidade.

---

## RNF07 — Manutenção

O CSS deverá utilizar Sass para facilitar manutenção e reaproveitamento.

---

# 13. Critérios de Sucesso

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

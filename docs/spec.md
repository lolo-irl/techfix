# Especificações Técnicas - TechFix

Documentação de especificação técnica, versionamento de tecnologias, contratos de APIs e parâmetros de desenvolvimento para a aplicação **TechFix**.

---

## 1. Framework CSS & UI

### Bootstrap
* **Versão Exata:** `v5.3.3`
* **Método de Integração:** NPM / CDN (`bootstrap.bundle.min.js` e `bootstrap.min.css`)
* **Licença:** MIT
* **Arquivos CSS/Sass:** Importação modular via Sass em `scss/style.scss` com sobrescrita de variáveis do framework.

### Recursos & Componentes Utilizados:
* **Sistema de Layout:** `Grid System` de 12 colunas com breakpoints padrão (`sm: 576px`, `md: 768px`, `lg: 992px`, `xl: 1200px`) e `Containers`.
* **Navegação:** `Navbar` responsiva com botão toggler e menu colapsável para telas menores.
* **Exibição de Conteúdo:** `Cards` responsivos para catalogação e listagem de serviços de manutenção.
* **Formulários:** Controles de formulário estilizados (`form-control`, `form-select`, `form-check`, `input-group`) com classes de validação e estados de erro/sucesso.
* **Componentes Interativos:** `Modal` para detalhes de serviços e confirmação de solicitação, além de alertas temporários (`Alerts`).
* **Utilitários:** Spacing (`m-*`, `p-*`), Flexbox (`d-flex`, `justify-content-*`, `align-items-*`), e tipografia adaptativa.

---

## 2. API Pública Integrada (ViaCEP)

A API pública **ViaCEP** é utilizada no formulário de solicitação de manutenção (`solicitar.html`) para consulta dinâmica de endereço a partir do CEP.

* **Nome do Serviço:** ViaCEP Webservice
* **Versão / Protocolo:** REST / HTTPS
* **URL Base:** `https://viacep.com.br/ws/`
* **Autenticação:** Não necessária (Open Access)
* **Formato de Comunicação:** `JSON`

### Contrato do Endpoint:
* **Endpoint:** `GET /{cep}/json/`
* **Parâmetro de Entrada:** `{cep}` (String contendo 8 dígitos numéricos, ex: `01001000` ou `01001-000`).

#### Exemplo de Resposta do Servidor (`200 OK`):
```json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "complemento": "lado ímpar",
  "bairro": "Sé",
  "localidade": "São Paulo",
  "uf": "SP",
  "ibge": "3550308",
  "gia": "1004",
  "ddd": "11",
  "siafi": "7107"
}

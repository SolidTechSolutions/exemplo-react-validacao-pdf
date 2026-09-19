# 🇧🇷 SolidSign API - Front-end de Exemplo: Validação de PDF/PAdES (React)

Este projeto é um front-end de exemplo para **validar documentos PDF assinados**. Por padrão fala com o back-end de exemplo [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf), que guarda as credenciais da API do lado do servidor — o padrão de integração recomendado pra clientes. Um modo opcional "Direct to SolidSign API" permite chamar a API diretamente do navegador, útil pra um teste manual rápido, mas expõe o token no browser.

O relatório exibido é propositalmente simples (uma tabela com os campos principais), não uma réplica da interface do validador do Portal SolidSign.

## Como funciona

- **Modo padrão (backend)**: `POST http://localhost:8094/api/pdf/validate/form` — o backend de exemplo repassa pra SolidSign API usando as credenciais do seu `application.properties`.
- **Modo opcional (direto)**: `POST {baseUrl}/solidsign/dsig/validation/verify-pdf` — direto do navegador, com o token informado no formulário.

> **Nota:** a partir de setembro de 2026, o modo direto só funciona se a origem do seu front-end estiver na allow-list de CORS da API (`solidsign.cors.allowed-origins`, que por padrão só inclui os domínios do Portal SolidSign). Testar contra a API de produção a partir de `localhost` vai dar 403 — use o modo padrão (backend) em vez disso.

## Pré-requisitos

1. Rode o back-end [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf) localmente (`mvn spring-boot:run`, porta padrão `8094`) — ou, se for usar o modo direto, tenha um token JWT válido.
2. Um ou mais PDFs assinados (PAdES) para validar.

## Rodando

```bash
npm install
npm run dev
```

Abra `http://localhost:5173`, envie o(s) PDF(s) e valide.

---

# 🇬🇧 SolidSign API - Example Front-end: PDF/PAdES Validation (React)

This project is an example front-end for **validating signed PDF documents**. By default it talks to the [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf) example backend, which keeps the API credentials server-side — the recommended integration pattern for customers. An optional "Direct to SolidSign API" mode lets you call the API straight from the browser, useful for a quick manual check, but it exposes the token in the browser.

The displayed report is intentionally plain (a table of key fields), not a reproduction of the Portal SolidSign validator's UI.

## How it works

- **Default mode (backend)**: `POST http://localhost:8094/api/pdf/validate/form` — the example backend forwards to the SolidSign API using the credentials from its own `application.properties`.
- **Optional mode (direct)**: `POST {baseUrl}/solidsign/dsig/validation/verify-pdf` — straight from the browser, with the token entered in the form.

> **Note:** as of September 2026, direct mode only works if your front-end's origin is on the SolidSign API's CORS allow-list (`solidsign.cors.allowed-origins`, which by default only includes the Portal SolidSign domains). Testing against the production API from `localhost` will get a 403 — use the default (backend) mode instead.

## Prerequisites

1. Run the [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf) backend locally (`mvn spring-boot:run`, default port `8094`) — or, for direct mode, have a valid JWT token.
2. One or more signed (PAdES) PDFs to validate.

## Running

```bash
npm install
npm run dev
```

Open `http://localhost:5173`, upload the PDF(s) and validate.

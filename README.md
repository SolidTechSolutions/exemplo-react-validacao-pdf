# 🇧🇷 SolidSign API - Front-end de Exemplo: Validação PDF (React)

## Como funciona

"Via example backend" (padrão) chama `POST /api/pdf/validate/form` no back-end de exemplo (`http://localhost:8094`), que repassa pra `POST /solidsign/dsig/validation/verify-pdf` da SolidSign API e nunca expõe seu token no navegador. "Direct to SolidSign API" (opcional) chama a API direto do navegador — só pra teste manual rápido.

## Requisitos

Rode **um** destes back-ends de exemplo localmente (todos implementam o mesmo endpoint de formulário e a mesma porta padrão usada abaixo):

- **Java**: [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf)
- **C#**: [`exemplo-csharp-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-csharp-integracao-validacao-pdf)
- **TypeScript**: [`exemplo-typescript-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-typescript-integracao-validacao-pdf)
- **Python**: [`exemplo-python-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-python-integracao-validacao-pdf)
- **PHP**: [`exemplo-php-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-php-integracao-validacao-pdf)
- **Node.js**: [`exemplo-nodejs-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-nodejs-integracao-validacao-pdf)
- **JavaScript**: [`exemplo-javascript-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-javascript-integracao-validacao-pdf)

- Um token JWT válido (`POST /solidsign/auth/token`)
- Recomendado pra produção: o modo "via backend" — a credencial nunca sai do servidor.

## Como rodar

```bash
npm install
npm run dev
```

Abra `http://localhost:5173`, preencha o formulário e envie.

## Variáveis do formulário

| Campo | Significado | Default |
|---|---|---|
| `mode` | Via backend de exemplo (padrão) ou direto à API | `backend` |
| `backendUrl` | URL do back-end de exemplo | `http://localhost:8094` |
| `authorization` | Token JWT (Bearer) — só usado no modo "direct" | (vazio) |
| `documents` | Documento(s) assinado(s) a validar | (vazio) |

---

# 🇬🇧 SolidSign API - Example Front-end: PDF Validation (React)

## How it works

"Via example backend" (default) calls `POST /api/pdf/validate/form` on the example backend (`http://localhost:8094`), which forwards to `POST /solidsign/dsig/validation/verify-pdf` on the SolidSign API and never exposes your token in the browser. "Direct to SolidSign API" (optional) calls the API straight from the browser — for quick manual testing only.

## Requirements

Run **one** of these example backends locally (all implement the same form endpoint and default port used below):

- **Java**: [`exemplo-java-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-java-integracao-validacao-pdf)
- **C#**: [`exemplo-csharp-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-csharp-integracao-validacao-pdf)
- **TypeScript**: [`exemplo-typescript-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-typescript-integracao-validacao-pdf)
- **Python**: [`exemplo-python-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-python-integracao-validacao-pdf)
- **PHP**: [`exemplo-php-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-php-integracao-validacao-pdf)
- **Node.js**: [`exemplo-nodejs-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-nodejs-integracao-validacao-pdf)
- **JavaScript**: [`exemplo-javascript-integracao-validacao-pdf`](https://github.com/SolidTechSolutions/exemplo-javascript-integracao-validacao-pdf)

- A valid JWT token (`POST /solidsign/auth/token`)
- Recommended for production: "via backend" mode — the credential never leaves the server.

## Running

```bash
npm install
npm run dev
```

Open `http://localhost:5173`, fill in the form and submit.

## Form fields

| Field | Meaning | Default |
|---|---|---|
| `mode` | Via example backend (default) or direct to API | `backend` |
| `backendUrl` | Example backend URL | `http://localhost:8094` |
| `authorization` | JWT (Bearer) token — only used in "direct" mode | (empty) |
| `documents` | Signed document(s) to validate | (empty) |

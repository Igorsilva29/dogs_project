# Dogs

<p align="center">
  <img src="./src/Assets/dogs.svg" alt="Dogs logo" width="120" />
</p>

<p align="center">
  Rede social para cachorros — projeto do curso de <strong>React</strong> da <a href="https://www.origamid.com/">Origamid</a>.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Vite-8-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/React_Router-7-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white" alt="React Router" />
  <img src="https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
</p>

---

## Sobre o projeto

O **Dogs** é uma aplicação front-end de rede social voltada a fotos de cachorros. O app consome a [Dogs API](https://dogsapi.origamid.dev/json) da Origamid e cobre autenticação JWT, contexto de usuário, formulários com validação e rotas protegidas.

---

## Stack

| Tecnologia | Uso no projeto |
| :--- | :--- |
| ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) | UI com componentes funcionais e hooks |
| ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) | Bundler e servidor de desenvolvimento |
| ![React Router](https://img.shields.io/badge/React_Router-CA4245?style=flat-square&logo=reactrouter&logoColor=white) | Navegação e rotas (`/`, `/login/*`) |
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) | Linguagem principal do app |
| ![CSS Modules](https://img.shields.io/badge/CSS_Modules-1572B6?style=flat-square&logo=css3&logoColor=white) | Estilos isolados por componente |
| ![SVGR](https://img.shields.io/badge/vite--plugin--svgr-FFB13B?style=flat-square&logo=svg&logoColor=black) | SVG importado como componente React |
| ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white) | Lint e boas práticas |
| ![Prettier](https://img.shields.io/badge/Prettier-F7B93E?style=flat-square&logo=prettier&logoColor=black) | Formatação de código |
| ![Fetch API](https://img.shields.io/badge/Fetch_API-000000?style=flat-square&logo=firefox&logoColor=white) | Requisições HTTP à Dogs API |
| ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) | Autenticação via token |

---

## Funcionalidades

- Login e persistência de sessão com JWT no `localStorage`
- Contexto global de usuário (`UserContext`)
- Validação de formulários com hook customizado (`useForm`)
- Rotas de login, cadastro, recuperar e resetar senha
- Header dinâmico conforme estado de autenticação
- Consumo da API REST da Origamid

---

## Como rodar

### Pré-requisitos

- ![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=flat-square&logo=nodedotjs&logoColor=white) Node.js 18+  
- npm

### Instalação

```bash
npm install
```

### Desenvolvimento

```bash
npm run dev
```

Abra [http://localhost:5173](http://localhost:5173).

### Build de produção

```bash
npm run build
npm run preview
```

### Lint

```bash
npm run lint
```

---

## Estrutura

```text
src/
├── Assets/           # SVGs e imagens
├── Components/
│   ├── Forms/        # Input, Button
│   ├── Login/        # Login, cadastro, senha
│   ├── Header.jsx
│   ├── Footer.jsx
│   └── Home.jsx
├── Hooks/
│   └── useForm.jsx   # Validação de campos
├── api.jsx           # Endpoints da Dogs API
├── UserContext.jsx   # Estado global do usuário
├── App.jsx
└── index.jsx
```

---

## API

Base URL:

```text
https://dogsapi.origamid.dev/json
```

Endpoints usados no projeto:

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `POST` | `/jwt-auth/v1/token` | Login (obter token) |
| `POST` | `/jwt-auth/v1/token/validate` | Validar token |
| `GET` | `/api/user` | Dados do usuário autenticado |

> Conta de teste comum no curso: usuário `dog` / senha `dog`

---

## Scripts

| Comando | Descrição |
| :--- | :--- |
| `npm run dev` | Sobe o servidor Vite |
| `npm run build` | Gera o build de produção |
| `npm run preview` | Preview do build |
| `npm run lint` | Roda o ESLint |

---

## Créditos

Projeto desenvolvido acompanhando o curso **React Completo** da [Origamid](https://www.origamid.com/).

<p align="center">
  <img src="https://img.shields.io/badge/Feito_com-React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="Feito com React" />
</p>

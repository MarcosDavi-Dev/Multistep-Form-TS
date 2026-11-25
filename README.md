# Multistep React + TypeScript

🌐 **Demo / Demonstração:** [https://multistep-react-ts.web.app](https://multistep-react-ts.web.app/)

[🇧🇷 Português](#-português) | [🇺🇸 English](#-english)

---

## 🇧🇷 Português

### Sobre o projeto

Formulário de avaliação de produto dividido em **etapas** (multistep), construído com **React** e **TypeScript**. O usuário se identifica, avalia o produto com emojis e comentário, e recebe uma tela de agradecimento ao final. Os dados preenchidos são mantidos ao navegar entre as etapas.

### Funcionalidades

- Navegação entre etapas: **Identificação → Avaliação → Envio**
- Indicador visual de progresso com ícones
- Botões **Voltar** e **Avançar**
- Persistência dos dados ao navegar entre as etapas (estado centralizado)
- Avaliação por emojis: _Insatisfeito_, _Poderia ser melhor_, _Satisfeito_ e _Muito satisfeito_
- Campo de comentário
- Tela de agradecimento

### Ferramentas utilizadas

| Ferramenta                                                   | Para que serve no projeto                                      |
| ------------------------------------------------------------ | -------------------------------------------------------------- |
| [Vite](https://vite.dev/)                                    | Criação do projeto, servidor de desenvolvimento e build rápido |
| [React](https://react.dev/)                                  | Construção da interface com componentes e hooks                |
| [TypeScript](https://www.typescriptlang.org/)                | Tipagem estática (props, estado e eventos)                     |
| [React Icons](https://react-icons.github.io/react-icons/)    | Ícones do indicador de etapas e dos emojis de avaliação        |
| [ESLint](https://eslint.org/)                                | Padronização e análise estática do código                      |
| CSS                                                          | Estilização dos componentes                                    |
| [Firebase Hosting](https://firebase.google.com/docs/hosting) | Publicação da aplicação                                        |

### Conceitos aplicados

- **Hook customizado (`useForm`)**: controla a etapa atual e expõe `currentStep`, `currentComponent`, `changeStep`, `isFirstStep` e `isLastStep`.
- **Estado centralizado no `App`**: um único objeto (`FormFields`) guarda `name`, `email`, `review` e `comment`, repassado aos componentes por props.
- **Inputs controlados** e função `updateFieldHandler` tipada com `keyof FormFields`.
- **`verbatimModuleSyntax`**: importação de tipos com `import type`.
- Uso de tipos de evento atuais (`SubmitEvent`) no lugar de tipos preteridos (`FormEvent`).

### Estrutura de pastas

```
src/
├── components/
│   ├── ReviewForm.tsx   # Etapa de avaliação (emoji + comentário)
│   ├── Steps.tsx        # Indicador de etapas
│   ├── Thanks.tsx       # Tela de agradecimento
│   └── UserForm.tsx     # Etapa de identificação (nome e e-mail)
├── hooks/
│   └── useForm.ts       # Hook de controle das etapas
├── App.tsx
├── App.css
├── index.css
└── main.tsx
```

### Como executar

```bash
# Clone o repositório
git clone <URL-DO-SEU-REPOSITORIO>
cd <NOME-DA-PASTA>

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev

# Gere a build de produção
npm run build
```

### Deploy no Firebase

```bash
npm install -g firebase-tools
firebase login
npm run build
firebase deploy
```

---

## 🇺🇸 English

### About the project

A product review form split into **steps** (multistep), built with **React** and **TypeScript**. The user identifies themselves, rates the product with emojis and a comment, and sees a thank-you screen at the end. The data entered is preserved while navigating between steps.

### Features

- Step navigation: **Identification → Review → Submit**
- Visual progress indicator with icons
- **Back** and **Next** buttons
- Data persistence across steps (centralized state)
- Emoji rating: _Unsatisfied_, _Could be better_, _Satisfied_ and _Very satisfied_
- Comment field
- Thank-you screen

### Tools

| Tool                                                         | Purpose in the project                             |
| ------------------------------------------------------------ | -------------------------------------------------- |
| [Vite](https://vite.dev/)                                    | Project scaffolding, dev server and fast builds    |
| [React](https://react.dev/)                                  | UI built with components and hooks                 |
| [TypeScript](https://www.typescriptlang.org/)                | Static typing (props, state and events)            |
| [React Icons](https://react-icons.github.io/react-icons/)    | Icons for the step indicator and the rating emojis |
| [ESLint](https://eslint.org/)                                | Code linting and consistency                       |
| CSS                                                          | Component styling                                  |
| [Firebase Hosting](https://firebase.google.com/docs/hosting) | Application deployment                             |

### Concepts applied

- **Custom hook (`useForm`)**: controls the current step and exposes `currentStep`, `currentComponent`, `changeStep`, `isFirstStep` and `isLastStep`.
- **Centralized state in `App`**: a single object (`FormFields`) holds `name`, `email`, `review` and `comment`, passed down to components via props.
- **Controlled inputs** and an `updateFieldHandler` function typed with `keyof FormFields`.
- **`verbatimModuleSyntax`**: type imports with `import type`.
- Current event types (`SubmitEvent`) instead of deprecated ones (`FormEvent`).

### Folder structure

```
src/
├── components/
│   ├── ReviewForm.tsx   # Review step (emoji + comment)
│   ├── Steps.tsx        # Step indicator
│   ├── Thanks.tsx       # Thank-you screen
│   └── UserForm.tsx     # Identification step (name and email)
├── hooks/
│   └── useForm.ts       # Step control hook
├── App.tsx
├── App.css
├── index.css
└── main.tsx
```

### Getting started

```bash
# Clone the repository
git clone <YOUR-REPOSITORY-URL>
cd <FOLDER-NAME>

# Install dependencies
npm install

# Start the development server
npm run dev

# Create the production build
npm run build
```

### Deploying to Firebase

```bash
npm install -g firebase-tools
firebase login
npm run build
firebase deploy
```

---

## 📄 License / Licença

Add your license here / Adicione sua licença aqui.

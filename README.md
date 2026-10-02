# Node-app-template

Starter template for Node.js services in TypeScript. It is the baseline I start backend services from, so the tooling is already wired before the first feature is written.

## What is included

- **Express** app split into `src/app.ts` (the app) and `src/server.ts` (the listener), so tests can import the app without opening a port
- **Config** loaded from `.env.<NODE_ENV>` through a single `Config` object
- **Winston** logger
- **Jest** with ts-jest and Supertest, with a sample spec in `app.spec.ts`
- **ESLint** and **Prettier**
- **Husky** pre-commit hook running lint-staged
- `.nvmrc` to pin the Node.js version

## Getting started

```bash
git clone https://github.com/Nur-Adnan/Node-app-template.git my-service
cd my-service
npm install
```

Create `.env.dev` (see `.env.example`):

```env
PORT=5501
NODE_ENV=dev
```

```bash
npm run dev
```

Before building on it, change `name`, `description` and `author` in `package.json`.

## Scripts

| Script | Purpose |
|---|---|
| `npm run dev` | Start with nodemon and `NODE_ENV=dev` |
| `npm run build` | Compile TypeScript |
| `npm test` | Jest with coverage |
| `npm run lint` / `lint:fix` | ESLint |
| `npm run format:check` / `format:fix` | Prettier |

## Used by

[micro-auth-service](https://github.com/Nur-Adnan/micro-auth-service) was started from this template.

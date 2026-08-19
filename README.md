# WS101 — Week 3 Laboratory: Typed Hooks & State

A React + TypeScript + Vite implementation of the WS101 Week 3 laboratory.

## Laboratory objectives

This project demonstrates:

1. A generic `useFetch<T>` hook.
2. A public REST API call with TypeScript type safety.
3. A discriminated union for idle/loading/success/error states.
4. `useReducer` with typed actions for todo state.
5. A typed React Context provider for light/dark theme switching.
6. TypeScript narrowing and strict type checking.

## API source

This project uses **JSONPlaceholder**:

`https://jsonplaceholder.typicode.com/todos`

The API response is typed as `Todo[]` using `src/types/api.ts`.

## Project structure

```text
src/
├── components/
│   ├── TodoApp.tsx
│   └── TodoList.tsx
├── contexts/
│   └── ThemeContext.tsx
├── hooks/
│   ├── todoReducer.ts
│   └── useFetch.ts
├── types/
│   └── api.ts
├── App.tsx
├── index.css
└── main.tsx
```

## Setup

Requirements: Node.js and npm.

```bash
npm install
npm run dev
```

Open the local Vite URL shown in the terminal.

## Verify type safety

Run:

```bash
npx tsc --noEmit
```

Expected result: **zero TypeScript errors**.

You can also run the production build:

```bash
npm run build
```

## Features to demonstrate in screenshots

For the laboratory submission, capture:

- **TodoList / fetch:** the JSONPlaceholder todos loaded successfully.
- **TodoApp / reducer:** add a todo, toggle it, delete it, and switch between All / Active / Completed filters.
- **Theme context:** switch between Light Mode and Dark Mode.
- **Type checking:** terminal showing `npx tsc --noEmit` with no errors.

## Reflection

Discriminated unions make asynchronous states predictable because the `status` field tells TypeScript which properties are available, so `data` and `error` are accessed only in their valid states. Generics make `useFetch<T>` reusable while keeping the fetched response strongly typed at each call site.

## GitHub submission

After creating the repository on GitHub:

```bash
git init
git add .
git commit -m "Week 3 Lab - Typed Hooks & State"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ws101-lab3.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

## Laboratory source

Based on the supplied **WS101 — Web Systems and Technologies 1, Week 3 Laboratory: Typed Hooks & State** instructions.
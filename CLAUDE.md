# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

React 19 + TypeScript + Vite 7 application.

## Commands

- `npm run dev` — Start dev server with HMR
- `npm run build` — Type-check with `tsc -b` then build with Vite
- `npm run lint` — ESLint across all .ts/.tsx files
- `npm run preview` — Preview production build locally

## Architecture

- **Entry point**: `index.html` → `src/main.tsx` → `src/App.tsx`
- **Static assets**: `public/` (served as-is), `src/assets/` (processed by Vite)
- **Styling**: CSS files co-located with components (`App.css`) plus global styles (`index.css`)

## TypeScript

- Strict mode enabled with `noUnusedLocals` and `noUnusedParameters`
- JSX transform: `react-jsx` (no React import needed in components)
- Two tsconfig files: `tsconfig.app.json` (app code, ES2022) and `tsconfig.node.json` (Vite config, ES2023)

## Lint

- ESLint flat config format (`eslint.config.js`)
- Plugins: typescript-eslint, react-hooks, react-refresh

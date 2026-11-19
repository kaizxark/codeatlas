# CodeAtlas

CodeAtlas is an interactive codebase dependency explorer for JavaScript and TypeScript projects. It parses repository structure and imports into a navigable graph so developers can inspect module relationships, follow dependency paths, and reason about change impact before editing code.

## What is included

This repository contains the complete application source, including:

- Next.js App Router pages and server-side application logic
- TypeScript AST parsing and dependency-graph generation
- Interactive graph analysis and module detail views
- Repository insights, route tables, and analysis summaries
- AI-assisted explanations backed by parsed repository structure
- Authentication and organization-aware application flows
- Supabase data access and row-level security integration points
- Tailwind CSS styling and reusable interface components
- Command-line analysis scripts for parsing, map counts, insights, and deeper analysis

## Technology

The project uses Next.js, React, TypeScript, Tailwind CSS, `ts-morph`, React Flow, Dagre, Clerk, Supabase, OpenAI, and LangSmith. Dependency versions are defined in [`package.json`](./package.json) and the workspace lockfile.

## Requirements

- Node.js
- pnpm 10 or newer
- Credentials for the services enabled in your environment: Clerk, Supabase, OpenAI, LangSmith, and the optional analysis agent

## Local setup

```bash
pnpm install
cp .env.example .env.local
pnpm dev
```

Open `http://localhost:3000` after the development server starts.

Available scripts:

```bash
pnpm dev
pnpm build
pnpm start
pnpm lint
pnpm parse
pnpm map-counts
pnpm insights
pnpm analyze
```

Review [`.env.example`](./.env.example) before running service-backed features. Do not commit secrets or populated environment files.

## Project layout

- `app/` — application routes and global styles
- `components/` — interactive analysis interface and reusable UI
- `lib/` — environment, roles, theme, graph, parser, pipeline, and service helpers
- `scripts/` — repository parsing and analysis commands
- `supabase/` — database migrations
- `docs/` — project documentation and specifications
- `types/` — shared TypeScript declarations
- `public/` — static assets

## Source attribution

CodeAtlas is a renamed project repository containing the source code from [adrianhajdin/cartograph](https://github.com/adrianhajdin/cartograph). The original project and its authors retain their applicable rights and notices. This README is original to CodeAtlas; consult the source files and upstream repository for additional provenance and licensing information.

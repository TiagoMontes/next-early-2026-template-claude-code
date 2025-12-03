# Next.js Early 2026 Template

A modern Next.js template repository featuring the latest stable versions and best practices for early 2026.

## Technology Stack

- **Next.js** 16.0.6 with App Router
- **React** 19.2.0
- **TypeScript** 5
- **Tailwind CSS** v4 with @tailwindcss/postcss
- **ESLint** 9 with flat config
- **Package Manager**: Bun
- **Fonts**: Geist Sans & Geist Mono

## Getting Started

### Use This Template

Click the "Use this template" button on GitHub to create a new repository from this template.

### Installation

```bash
bun install
```

### Development

```bash
bun dev
```

Open [http://localhost:3000](http://localhost:3000) to see your application.

### Build

```bash
bun run build
bun start
```

### Linting

```bash
bun run lint
```

## Project Structure

```
├── app/
│   ├── layout.tsx      # Root layout with fonts and metadata
│   ├── page.tsx        # Home page
│   └── globals.css     # Global styles and Tailwind imports
├── public/             # Static assets
└── CLAUDE.md          # Instructions for Claude Code
```

## Features

- Modern App Router architecture
- TypeScript with path aliases (`@/*`)
- Tailwind CSS v4 with CSS variables for theming
- Dark mode support via `prefers-color-scheme`
- Optimized font loading with next/font
- ESLint configuration with Next.js best practices
- Fast package management with Bun

## Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Tailwind CSS v4](https://tailwindcss.com/docs)
- [TypeScript](https://www.typescriptlang.org/docs)
- [Bun](https://bun.sh/docs)

## Deploy

Deploy easily on [Vercel](https://vercel.com/new) or any platform that supports Next.js.

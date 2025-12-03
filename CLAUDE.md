# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Technology Stack

- **Framework**: Next.js 16.0.6 (App Router)
- **Runtime**: React 19.2.0
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS v4 (with @tailwindcss/postcss)
- **Fonts**: Geist Sans & Geist Mono (via next/font/google)
- **Linting**: ESLint 9 with eslint-config-next

## Development Commands

```bash
# Start development server (runs at http://localhost:3000)
npm run dev

# Build for production
npm run build

# Start production server
npm run start

# Run linting
npm run lint
```

## Project Structure

This is a Next.js App Router application with the following structure:

- **app/**: Main application directory using App Router architecture
  - `layout.tsx`: Root layout with font configuration and metadata
  - `page.tsx`: Home page component
  - `globals.css`: Global styles with Tailwind CSS imports and CSS variables
- **public/**: Static assets (next.svg, vercel.svg, etc.)
- **TypeScript**: Path alias `@/*` maps to root directory

## Architecture Notes

### Styling System

- Uses **Tailwind CSS v4** with the new `@tailwindcss/postcss` plugin
- CSS variables are defined in `globals.css` for theming:
  - `--background` and `--foreground` with dark mode support via `prefers-color-scheme`
  - Theme tokens are mapped using Tailwind's `@theme inline` directive
- Font variables (`--font-geist-sans`, `--font-geist-mono`) are injected by Next.js font loader

### Font Configuration

Fonts are configured in `app/layout.tsx` using next/font/google:
- Geist Sans (variable: `--font-geist-sans`)
- Geist Mono (variable: `--font-geist-mono`)
- Both fonts use the `latin` subset

### ESLint Configuration

Uses ESLint 9's flat config format (`eslint.config.mjs`):
- Includes `eslint-config-next/core-web-vitals` for Next.js best practices
- Includes `eslint-config-next/typescript` for TypeScript rules
- Global ignores: `.next/**`, `out/**`, `build/**`, `next-env.d.ts`

### Next.js Configuration

The `next.config.ts` file is minimal with no custom configuration currently applied.

## Important Conventions

- This project uses **TypeScript** exclusively - do not create `.js` or `.jsx` files
- All React components should use TypeScript with proper type definitions
- The App Router is used (not Pages Router) - pages go in the `app/` directory
- Use the `@/` path alias for imports from the root directory

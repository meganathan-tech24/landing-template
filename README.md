# Landing Template

A modern, fully responsive marketing/landing page template built with Next.js, TypeScript, and Tailwind CSS — designed as a reusable foundation for SaaS, agency, or product marketing sites.

![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3.x-38B2AC?logo=tailwind-css)
![License](https://img.shields.io/badge/license-MIT-green)

**[Live Demo](#)** · **[Report Bug](#)** · **[Request Feature](#)**

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Available Scripts](#available-scripts)
- [Customization](#customization)
- [Deployment](#deployment)
- [Performance & Accessibility](#performance--accessibility)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Overview

This template provides a production-ready marketing site skeleton with a fully componentized section-based architecture. It's built to be cloned, re-themed, and shipped — copy is centralized in a single config file, so rebranding the entire site takes minutes, not hours.

## Features

- **Fully responsive** — mobile-first layout tested across breakpoints
- **Dark / light mode** — system-aware theme toggle
- **Section-based architecture** — Hero, Features, Pricing, Testimonials, FAQ, CTA, Footer as isolated, reusable components
- **Centralized content layer** — all copy lives in `lib/content.ts`, decoupled from UI
- **Accessible by default** — semantic HTML, keyboard navigation, ARIA-compliant shadcn/ui primitives
- **Scroll-triggered animations** — lightweight reveal-on-scroll wrapper, no heavy animation libraries
- **SEO-ready** — metadata API, Open Graph tags, sitemap & robots.txt included
- **Type-safe** — end-to-end TypeScript with strict mode enabled

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Next.js 14](https://nextjs.org/) (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS |
| UI Primitives | shadcn/ui |
| Icons | lucide-react |
| Linting/Formatting | ESLint, Prettier |
| Git Hooks | Husky, lint-staged, commitlint |
| CI | GitHub Actions |
| Deployment | Vercel |

## Project Structure

```
landing-template/
├── app/                    # Routes, layout, global styles
├── components/
│   ├── sections/           # Hero, Features, Pricing, FAQ, etc.
│   ├── layout/              # Navbar, ThemeToggle
│   ├── ui/                  # shadcn/ui primitives
│   └── shared/               # SectionHeading, AnimatedReveal, GradientBlob
├── lib/                    # utils.ts, content.ts (all copy/config)
├── config/                 # site.ts — nav, social, metadata
├── types/                  # Shared TypeScript interfaces
└── public/                 # Images, logos, favicon
```

## Getting Started

### Prerequisites

- Node.js `>=18.17` (see `.nvmrc`)
- npm, pnpm, or yarn

### Installation

```bash
git clone https://github.com/<your-username>/landing-template.git
cd landing-template
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view it locally.

## Environment Variables

Create a `.env.local` file in the root directory:

```env
NEXT_PUBLIC_SITE_URL=http://localhost:3000
NEXT_PUBLIC_CONTACT_EMAIL=hello@example.com
```

See `.env.example` for the full list of supported variables.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start local dev server |
| `npm run build` | Production build |
| `npm run start` | Serve production build |
| `npm run lint` | Run ESLint |
| `npm run format` | Run Prettier |
| `npm run typecheck` | Run TypeScript compiler checks |

## Customization

1. **Branding** — update `config/site.ts` with your site name, logo, and social links
2. **Copy** — edit `lib/content.ts` to change all section text, pricing tiers, testimonials, and FAQ items
3. **Theme** — adjust CSS variables in `app/globals.css` and `tailwind.config.ts` for colors, radii, and fonts
4. **Sections** — add, remove, or reorder sections directly in `app/page.tsx`

## Deployment

This project is optimized for [Vercel](https://vercel.com):

```bash
npm i -g vercel
vercel
```

Alternatively, build and deploy the static output to any Node-compatible host:

```bash
npm run build
npm run start
```

## Performance & Accessibility

- Lighthouse scores targeted at 95+ across Performance, Accessibility, Best Practices, and SEO
- Images optimized via `next/image`
- Semantic landmarks (`<header>`, `<main>`, `<footer>`) and skip-to-content link included

## Roadmap

- [ ] Add CMS integration option (Sanity/Contentful)
- [ ] Add i18n support
- [ ] Add Storybook for component documentation
- [ ] Add unit tests (Vitest + Testing Library)

See [open issues](#) for the full list of proposed features.

## Contributing

Contributions are welcome. Please follow the existing commit convention ([Conventional Commits](https://www.conventionalcommits.org/)):

```bash
git checkout -b feat/your-feature
git commit -m "feat: add pricing toggle animation"
git push origin feat/your-feature
```

Then open a pull request against `main`.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Built by **Meganathan** — Full-Stack Developer (React/TypeScript, Node.js/Express/Prisma)

- Portfolio: [your-portfolio-url]
- Upwork: [your-upwork-profile]
- Fiverr: [@meganathan248](#)

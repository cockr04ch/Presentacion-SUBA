# GEMINI.md - Proyecto SUBA (Presentation)

## Project Overview
This project is a professional slide deck for **Proyecto SUBA - Refactorización v2.0**, created using [Slidev](https://sli.dev/). SUBA (Sistema Automatizado de Boletería Urbana) is an integrated platform for modernizing urban transport in Ciudad Bolívar, Venezuela, connecting passengers and drivers.

### Presentation Highlights
- **Module Overview:** Passenger (Real-time tracking, QR/NFC payments) and Driver (Payment reception, location transmission).
- **Technology Stack (Application):** React Native (Expo SDK 54), MongoDB, Supabase (Storage), Node.js (API).
- **Architecture (v2.0):** Shift to a Data-Driven model with dynamic routes, real-time stops, and GeoJSON rendering.
- **Workflow:** Gitflow methodology (PR-based, feature naming conventions).

### Core Technologies (Presentation)
- **Framework:** Slidev (Vue 3 based)
- **Theme:** `seriph`, `default`
- **Highlighter:** Shiki
- **Deployment:** Configured for Netlify and Vercel

---

## Building and Running

The project uses `pnpm` as the primary package manager.

| Task | Command | Description |
| :--- | :--- | :--- |
| **Install** | `pnpm install` | Install dependencies. |
| **Development** | `pnpm dev` | Start the local development server with auto-reload. |
| **Build** | `pnpm build` | Build the presentation for production (outputs to `dist/`). |
| **Export** | `pnpm export` | Export the slides (e.g., to PDF). |

---

## Project Structure & Conventions

### Key Directories
- `slides.md`: The main entry point for the presentation content.
- `components/`: Custom Vue components used within slides (e.g., `Counter.vue`).
- `pages/`: Additional Markdown files for imported slides (e.g., `imported-slides.md`).
- `snippets/`: Code snippets for demonstration (e.g., `external.ts`).
- `public/`: Assets like `logotipo.png`.

### Development Conventions
- **Slide Authoring:** Content is written in Markdown with Frontmatter for styling and configuration.
- **Custom Logic:** Use Vue 3 components in `components/` for interactive slide elements.
- **Naming:** Follow the Gitflow convention mentioned in the slides: `feature/INITIALS/short-task` (e.g., `feature/JC/login-google`).
- **Commits:** No direct commits to `main`; use Pull Requests.

---

## Deployment
- **Netlify:** Configured via `netlify.toml` (node 20, `dist` folder).
- **Vercel:** Configured via `vercel.json` (`dist` folder).
- **Static Hosting:** The `build` command generates a static `dist/` folder that can be hosted on any static provider.

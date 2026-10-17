# Hi, I'm Adarsh 👋

**Frontend Engineer (SDE II) at Bajaj Finserv Health, Pune.** I build large-scale React and Next.js applications for enterprise B2B SaaS, with a focus on scalable UI architecture, microfrontends and web performance.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adarshkushwaha/)
[![Portfolio](https://img.shields.io/badge/Portfolio-adarshkushwaha.me-111?style=flat-square)](https://adarshkushwaha.me/)
[![Email](https://img.shields.io/badge/Email-adarshkushwaha296%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:adarshkushwaha296@gmail.com)
[![X](https://img.shields.io/badge/@heyadarshhere-000?style=flat-square&logo=x&logoColor=white)](https://x.com/heyadarshhere)

---

### At work

Nearly 4 years building production frontends for health and insurance B2B platforms used by enterprise clients:

- **Claims and booking platforms** handling **11,000+ claim submissions a day**, built with complex schema-driven forms and resilient async flows
- **Microfrontend architecture** with Module Federation: independently deployed apps, shared dependencies, and a reusable component system across products
- **Performance work** that took Lighthouse scores **from ~60 to 95** using SSR/SSG, code splitting, lazy loading and bundle optimization
- **AI voice-agent tooling:** campaign management and analytics UIs for voicebot workflows processing **125K+ calls a month**, and currently a PaaS platform for AI agents
- **Canvas-based image editing tools** for in-product workflows

*Work code is proprietary. The projects below are personal ones you can read in full.*

---

### Featured projects

#### [Baaza](https://github.com/Adarsh-kushwaha/baaza) · [live demo](https://baaza.vercel.app)
An installable, Spotify-style PWA that brings 100+ independent Indian playlist and radio sites into one app.
- **Problem:** browsers hide refused iframes, so "will this site embed?" can't be detected on the client. A server route reads each site's CSP `frame-ancestors` / `X-Frame-Options` with a spec-aware, unit-tested parser and falls back to a new tab.
- **State without a library:** a typed `localStorage` store read through `useSyncExternalStore`. It's SSR-safe and syncs across tabs.
- **Platform:** Server Components feed, hand-written service worker for offline use, and Capacitor shells for background audio on iOS and Android.
- `Next.js 16` `React 19` `TypeScript (strict)` `Tailwind v4` `Vitest`

#### [Revigion](https://github.com/Adarsh-kushwaha/revigion)
A spaced-repetition revision tracker that schedules 5 revisions per question and sends push reminders in the user's timezone.
- **Correct dates:** scheduling is done in calendar space in the user's IANA timezone, so DST and UTC day boundaries can't drift.
- **Testable dispatch:** the notification dispatcher is runtime-agnostic. The same code is unit-tested in Vitest and runs in a Deno Edge Function, with idempotent per-slot sends.
- **Responsive UI:** optimistic create/rename/delete with rollback, plus a per-user stale-while-revalidate client cache.
- `Next.js 16` `React 19` `TypeScript` `Supabase (Postgres + RLS + pg_cron)` `FCM` `Vitest`

---

### Tech I work with

| Area | Tools |
| --- | --- |
| **Core** | React, Next.js (App Router, RSC, SSR/SSG), TypeScript, JavaScript, HTML, CSS |
| **Architecture** | Microfrontends (Module Federation), monorepos, reusable component systems, design systems |
| **State and data** | Zustand, Redux, TanStack Query, REST, GraphQL, optimistic updates |
| **UI** | Tailwind CSS, shadcn/ui, Material UI, React Hook Form, responsive and accessible UI |
| **Performance** | Core Web Vitals, Lighthouse, code splitting, lazy loading, bundle analysis |
| **Quality and tooling** | Jest, Vitest, ESLint, Vite, Webpack, Git, CI/CD |
| **Also** | Node.js, Express, Kafka integrations, LangChain / LangGraph |

---

### How I build

- **Components:** small, composable, typed at the boundary. Own state where it's used and keep server state in a cache, not in global stores.
- **Performance is a feature:** measure first (Lighthouse, bundle analysis), ship less JavaScript, and render on the server when it helps.
- **Accessible by default:** semantic HTML, keyboard paths and visible focus before visual polish.
- **Design for failure:** every async view has loading, empty, error and retry states.
- **Test what's easy to get wrong:** date math, state machines and critical user flows.

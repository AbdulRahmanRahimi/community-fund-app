# Community Fund App

> **Client project** · Built by [Rahimi Tech Solution](https://github.com/AbdulRahmanRahimi) · The source code is private to the client.

A private web app for a community in British Columbia whose members pay into a shared monthly fund and lend to one another **interest-free, by member vote**. It replaces the leader's hand-kept records.

## Features

- Monthly contributions with reminders
- Support requests and **member voting**
- Payouts approved by two officers, then tracked repayments
- Events and polls
- Applications from new members
- Push notifications
- Statements, exports and an audit log for the officers
- Installs on phones as an app (PWA), in English, with Dari and Pashto planned

## Engineering highlights

- Every money rule lives in PostgreSQL functions, and the app only calls them
- Row Level Security, scheduled jobs (pg_cron) and Realtime updates
- Quality gates: unit tests, a pgTAP database suite with race-condition checks, Playwright end-to-end tests on phone and desktop with accessibility (axe) checks, Lighthouse scores, and a scan of the production bundle for secrets
- CI with GitHub Actions

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | Next.js 16 (App Router, React 19, TypeScript), Tailwind CSS 4, next-intl, Web Push |
| Backend | Supabase: PostgreSQL, Row Level Security, Auth, Storage, Realtime, pg_cron |
| Testing | pgTAP, Playwright, axe, Lighthouse |
| Hosting | Vercel |

---

Designed, built and deployed by **Abdul Rahman Rahimi**.

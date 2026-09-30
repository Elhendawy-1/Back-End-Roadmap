# .NET Backend Developer Roadmap

An interactive roadmap website for learning .NET backend development, stage by stage.

**Live page:** <a href="https://elhendawy-1.github.io/Back-End-Roadmap/" target="_blank" rel="noopener">https://elhendawy-1.github.io/Back-End-Roadmap/</a>

> Note: All learning resources and coupon codes live only inside the website. This README describes the structure without publishing any course links, playlists, or codes.

## Description

This website provides a structured learning path for becoming a .NET Backend Developer. It organizes **9 stages — from computer science fundamentals to ASP.NET Core** — each with a description, resource count, and hand-picked resource cards, so you always know what to learn next.

Total: **9 stages / 20 resources + a dedicated coupons section**.

## Roadmap Stages

| # | Stage | What you will learn | Resources |
|---|-------|---------------------|-----------|
| 1 | Computer Science Fundamentals | Essential programming fundamentals for every programmer (Level 1). | 1 Main Course |
| 2 | C# Fundamentals | C# from zero, covering the language basics in depth. | 1 Main Course |
| 3 | C# Object-Oriented Programming | OOP in C#: classes, objects, inheritance, polymorphism, abstraction. | 1 Main Course |
| 4 | SQL | Database concepts, ERD, relational schema, DDL/DML, queries, joins, views, constraints, indexes, normalization on SQL Server, plus 5 design projects / 54 SQL problems for practice, and T-SQL (variables, control flow, error handling, transactions, stored procedures, functions, window functions, triggers, cursors, CTEs). | 4 resources: 2 Main, 1 Practice, 1 Alternative |
| 5 | SOLID Principles | The 5 SOLID principles with C# before/after examples, quizzes, homework, and DIP vs. DI comparison. Requires strong OOP. | 3 resources: 1 Main, 1 Alternative, 1 Practice |
| 6 | Design Patterns | Design patterns from two different instructors / playlists. | 2 resources: 1 Main, 1 Alternative |
| 7 | LINQ | Language Integrated Query (LINQ) in C#. | 1 Main Course |
| 8 | Entity Framework Core | Data access with EF Core: ORM concepts, LINQ-to-SQL translation, DbContext, querying, change tracking, CRUD, transactions, loading strategies. Requires SQL and ADO.NET knowledge. | 2 resources: 1 Main, 1 Alternative (paid) |
| 9 | ASP.NET Core | Building production-ready APIs: HTTP basics, configuration, dependency injection, middleware, routing, REST, controller and minimal APIs, security (JWT / Roles / Policies), Docker Compose, Clean Architecture with CQRS, testing, and a full shop project. | 5 resources: 1 Main (paid, recommended), 4 Alternatives including paid and free options |

Each stage shows a description, a resource count, a "Mark stage complete" toggle with a completed medallion, and its resource cards.

## Learning Resources

Every resource card shows, without exposing anything in this README:

- Course title and resource type: Main Course, Alternative, or Practice
- Paid / Free indicator
- Platform name as plain text
- Notes such as video counts or prerequisites, when known
- A clear action button that opens the course in a new tab
- A copyable coupon code, where one applies

All links open in a new tab with `rel="noopener noreferrer"`. Open the website to access the complete, up-to-date list.

## Coupons

A dedicated section inside the website holds discount codes for the instructor's paid courses, with one-tap copy buttons (English and Arabic instructions included).

Coupon values are only visible in the app — they are intentionally not listed here.

## Features

- Continue banner that names the next unfinished stage
- Login gate: username + password accounts with per-user progress
- Stage navigation with completed (✓), up-next (→), and upcoming (○) states
- Search across stages, descriptions, and resource cards (also filters coupons)
- "Mark stage complete" toggles with a completed medallion per stage
- Per-stage resource counts
- Balanced responsive card grids (1, 2, or 3 columns by resource count)
- Double-tap reset progress with confirmation
- Light mode and Night mode (follows system preference, remembers your choice)
- Sticky search toolbar on mobile, back-to-top button
- Smooth scrolling with reduced-motion support
- Fully responsive down to 360px with 44px touch targets
- Inline SVG logo with matching browser-tab favicon
- Print-friendly (hides navigation, tools, and buttons when printing)

## Progress System

Progress is a simple per-stage checklist stored in the browser's **localStorage**. Each logged-in user gets their own progress; accounts store passwords salted and SHA-256 hashed, never plaintext, and the session is remembered in the same browser. If you used the site before logging in, your existing shared progress is copied into your account once on first login. Theme choice is stored separately.

There is no server or database — clearing browser storage removes accounts, progress, and settings.

## Technology Stack

- One self-contained `index.html` file: HTML, CSS, and vanilla JavaScript
- No frameworks, no CSS/JS libraries (only the system font stack — no webfont download)
- Browser `localStorage` for accounts, progress, session, and theme
- Clipboard API for coupon copy buttons, with a manual-select fallback
- SHA-256 via `crypto.subtle` for password hashing, with a local fallback

## Project Structure

```text
.
├── index.html        # The entire website: markup, styles, data, and logic
└── README.md         # This file (overview only, no course links)
```

- To add or change a resource, edit the `S` data array in the `<script>` section.
- To add a coupon code, edit the `codes` array.
- Stage order defines navigation, Continue behavior, and saved progress — do not reorder stages without resetting stored progress.

## Run Locally

No build step and no server required:

1. Clone the repository.
2. Open `index.html` in a browser (double-click works).

## Usage

1. Sign up with a username and password (stored only in your browser), then log in.
2. Follow the Continue banner — it always points at your next unfinished stage.
3. Open a resource card button to start learning (links open in a new tab).
4. Tick "Mark stage complete" as you finish each stage; progress saves automatically.
5. Use search or the stage pills to jump around; switch Light/Night from the top bar.
6. Log out from the user chip next to Reset; Reset progress needs two taps and clears only your own progress.

## Contributing

- Do not reorder, rename, or remove stages (saved progress depends on their order).
- Only add resources and codes that were actually provided; never invent course details.
- Keep the single-file structure and avoid adding libraries.
- Never commit course URLs, playlist IDs, or coupon codes to this README — keep them only in `index.html`.
- Test both themes and a 360px viewport before submitting changes.

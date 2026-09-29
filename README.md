# .NET Backend Developer Roadmap

An interactive roadmap website for learning .NET backend development, stage by stage.

**Live page:** https://elhendawy-1.github.io/Back-End-Roadmap/

## Description

This website provides a structured learning path for students who want to become .NET Backend Developers. Instead of collecting links, it organizes concepts progressively — foundations first, then backend core skills, architecture, production practices, and a final capstone project — so you always know what to learn next.

## Main Goals

- Provide a structured .NET backend learning path.
- Help students understand what to learn next.
- Organize courses and learning resources in one place.
- Track learning progress per student.
- Make the learning journey simple and easy to follow.
- Provide both free and paid learning resources.
- Include practice resources and a real project where available.

## Roadmap Structure

The roadmap is organized into **23 stages** grouped into **5 visual phases**, with **97 checkable learning topics** in total.

> Note: 22 stages carry topic checklists (97 topics). Computer Science Fundamentals is a resource-only guide stage with no checklist.

| Phase | What it covers |
| --- | --- |
| 1. Foundations | Starting point: computer science basics, Git, the C# language, databases, LINQ, and SOLID principles. |
| 2. Backend Core | Building real APIs: communication protocols, REST, ASP.NET Core, ORM / Entity Framework Core, security with JWT, and API documentation. |
| 3. Architecture | Writing code that lasts: design patterns, the Result pattern, domain modeling, clean architecture, and CQRS. |
| 4. Production | Shipping with confidence: testing, performance, observability, Docker, and CI with GitHub Actions. |
| 5. Capstone | Putting it all together in one full real project (Mechanic Shop Workshop Management System). |

## Learning Resources

Stages that have resources show them inside the stage panel, grouped by type:

- **Main Course** — the recommended resource for the stage.
- **Alternative** — a different course covering the same stage.
- **Practice** — exercises and project-based practice.
- **Paid** — clearly marked paid courses.
- **Coupon** — coupon-based courses with a copyable code.

Resources come from YouTube, ProgrammingAdvices, and Udemy. The website itself contains the complete, up-to-date links — open any stage to see them. URLs are never shown as raw text; every resource has a clear action button (Start Course, Open Alternative, Start Practice, Get Course).

## Features

- Interactive roadmap with 23 stages and 97 topics.
- Topic completion checkboxes with per-stage progress indicators.
- Overall roadmap progress bar.
- Continue banner that points to the next recommended stage.
- Recommended learning path with current-stage highlighting.
- Search across stages, topics, and resources.
- Phase navigation with scroll highlighting.
- Slide-in stage panels with topics and resource cards.
- Dark mode and light mode (follows system preference by default).
- Responsive, mobile-friendly single-column layout (no horizontal scrolling).
- Login gate with per-user progress and logout.
- Reset progress (per user, with confirmation).
- Paid course indicators and a dedicated coupon section with copy buttons.

## Progress System

Progress is tracked per logged-in user:

- Each checked topic is stored under that user's account.
- Stage cards show completed/total topics and a progress bar.
- Each phase shows its own aggregate progress.
- The header shows overall completion across all 97 topics.

All data is stored in the browser's **localStorage** — accounts, sessions, theme preference, and progress never leave the device. There is no server or database. Clearing browser storage removes accounts and progress.

## Recommended Learning Path

The Continue banner and the highlighted "Up next" card follow a recommended learning order (for example: Computer Science Fundamentals → Git → C# → … → Capstone). This order only drives the suggestion — it does not renumber stages or change stored progress.

## Responsive Design

The layout adapts from large desktop screens down to 360px phones:

- Multi-column card grids on desktop, fewer columns on tablets.
- Single-column learning path on mobile with full-width touch-friendly buttons.
- Sticky controls wrap instead of overflowing; the stage panel becomes a full-screen sheet on small screens.

## Themes

- **Dark mode** (default) and **light mode**, switchable from the toolbar.
- Colors, contrast, cards, buttons, badges, and coupon components are styled for both themes.

## Technology Stack

- HTML5, CSS3, vanilla JavaScript — no frameworks, no CSS/JS libraries.
- Browser `localStorage` for accounts, sessions, theme, and progress.
- Web Crypto API (SHA-256) for password hashing, with a built-in fallback.
- The only external asset is the Inter font from Google Fonts.

## Project Structure

```text
.
├── index.html        # Page structure: login gate, header, controls, panels, modals
├── css/
│   └── styles.css    # Theme, layout, components, responsive breakpoints
└── js/
    ├── data.js       # Phases, stages, topics, resources, coupons, learning order
    └── app.js        # Rendering, auth, progress, search, panel, theme logic
```

- To add or change a resource, edit `js/data.js` only.
- To change the look, edit `css/styles.css` only.
- Stage indexes (`0–22`) and progress keys must stay stable — renumbering a stage would orphan existing users' saved progress.

## Run Locally

No build step and no server required:

1. Clone the repository.
2. Open `index.html` in a browser (double-click works).

## Usage

1. Sign up with a username and password (stored only in your browser), then log in.
2. The Continue banner shows where to start — click it to open the stage.
3. Work through topics, checking them off as you finish; progress saves automatically.
4. Use search or the phase pills to jump around; switch theme from the toolbar.
5. Log out from the user chip; use Reset Progress to start a stage list over.

## Contributing

- Keep stage indexes and topic order stable (progress keys depend on them).
- Do not invent durations, prerequisites, or course claims — only add resources that were actually provided.
- Mark paid resources as `paid` and coupon resources with their exact code.
- Test both themes and a 360px viewport before submitting changes.

## Notes on Resources

- All course links, titles, and the coupon code (`MT260928G2ANEW`) are used exactly as provided by the roadmap owner.
- The Udemy ASP.NET Core 10 link opens with its coupon applied; the code is also shown with a copy button.
- Stages without a provided resource yet display a "coming soon" placeholder.

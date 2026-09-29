# .NET Backend Developer Roadmap

An interactive roadmap website for learning .NET backend development, stage by stage.

**Live page:** <a href="https://elhendawy-1.github.io/Back-End-Roadmap/" target="_blank" rel="noopener">https://elhendawy-1.github.io/Back-End-Roadmap/</a>

## Description

This website provides a structured learning path for students who want to become .NET Backend Developers. It organizes nine stages — from computer science fundamentals to ASP.NET Core — each with hand-picked learning resources, so you always know what to learn next.

## Roadmap Stages

1. Computer Science Fundamentals
2. C# Fundamentals
3. C# Object-Oriented Programming
4. SQL
5. SOLID Principles
6. Design Patterns
7. LINQ
8. Entity Framework Core
9. ASP.NET Core

Each stage shows a description, a resource count, a "Mark stage complete" toggle, and its resource cards.

## Learning Resources

Every resource card shows:

- Course title and resource type: Main Course, Alternative, or Practice
- Paid/Free indicator
- Platform name (YouTube, ProgrammingAdvices, Udemy, Metigator)
- Notes such as video counts or prerequisites, when known
- A clear action button: Watch Course, Start Course, Practice, Open Alternative, or Get Course
- A copyable coupon code, where one applies

All links open in a new tab. The website itself contains the complete, up-to-date links.

## Coupons

A dedicated section holds coupon codes for Eng. Mohamed Abu Hadhoud's courses on programmingadvices.com, with one-tap copy buttons (English and Arabic instructions included).

## Features

- Continue banner that names the next unfinished stage
- Stage navigation with completed (✓), up-next (→), and upcoming (○) states
- Search across stages, descriptions, and resource cards
- "Mark stage complete" toggles with a completed medallion per stage
- Per-stage resource counts
- Balanced responsive card grids (1, 2, or 3 columns by resource count)
- Double-tap reset progress with confirmation
- Light mode and Night mode (follows system preference, remembers your choice)
- Sticky search toolbar on mobile, back-to-top button
- Smooth scrolling with reduced-motion support
- Fully responsive down to 360px with 44px touch targets
- Inline SVG logo with matching browser-tab favicon

## Progress System

Progress is a simple per-stage checklist stored in the browser's **localStorage** under the key `roadmap-progress-v1`. Theme choice is stored as `roadmap-theme`. There is no account, server, or database — clearing browser storage removes progress and settings.

## Technology Stack

- One self-contained `index.html` file: HTML, CSS, and vanilla JavaScript
- No frameworks, no CSS/JS libraries (the only external asset is the system font stack — no webfont download)
- Browser `localStorage` for progress and theme
- Clipboard API for coupon copy buttons, with a manual-select fallback

## Project Structure

```text
.
├── index.html        # The entire website: markup, styles, data, and logic
└── README.md         # This file
```

- To add or change a resource, edit the `S` data array in the `<script>` section.
- To add a coupon code, edit the `codes` array.
- Stage order defines navigation, Continue behavior, and saved progress — do not reorder stages without resetting stored progress.

## Run Locally

No build step and no server required:

1. Clone the repository.
2. Open `index.html` in a browser (double-click works).

## Usage

1. Follow the Continue banner — it always points at your next unfinished stage.
2. Open a resource card button to start learning (links open in a new tab).
3. Tick "Mark stage complete" as you finish each stage; progress saves automatically.
4. Use search or the stage pills to jump around; switch Light/Night from the top bar.
5. Reset progress needs two taps to confirm.

## Contributing

- Do not reorder, rename, or remove stages (saved progress depends on their order).
- Only add resources and codes that were actually provided; never invent course details.
- Keep the single-file structure and avoid adding libraries.
- Test both themes and a 360px viewport before submitting changes.

## Notes on Resources

- Course titles, notes, links, and coupon codes are used exactly as provided.
- The Udemy ASP.NET Core 10 link opens with its coupon applied; the code is also shown with a copy button.
- Some cards honestly state "Content not checked" or "Lesson list not visible" where the source page could not be read.

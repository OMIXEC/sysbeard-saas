# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added
- GitHub-friendly `README.md` structure (overview, features, setup, deployment).
- UI/UX roadmap section in `README.md`.
- `.env.example` to document required environment variables for local setup.

### Fixed
- README Markdown formatting (broken sections/code fences).

## Roadmap (in progress)

This is a living plan for upcoming work. Items may move between phases as priorities shift.

### UI/UX
- [ ] Design tokens (spacing/typography/radii) applied consistently across core screens
- [ ] Standardize forms, buttons, modals (focus states + validation)
- [ ] Improve theme contrast/readability (WCAG-focused pass)
- [ ] Consistent empty states + loading skeletons for data-heavy views
- [ ] Booking flow polish (clear steps, time-slot UX, inline validation)
- [ ] Messaging UX (unread states, quicker navigation, better composer ergonomics)
- [ ] Accessibility pass (keyboard nav + visible focus rings)
- [ ] RTL regression pass (Arabic) across breakpoints
- [ ] Mobile/tablet improvements for calendar + booking management

### Performance & reliability
- [ ] Virtualize long lists where needed (`@tanstack/react-virtual`)
- [ ] Reduce chart rendering cost on large datasets (pagination/aggregation)
- [ ] Add lightweight error boundaries + consistent user-facing error states

### Security & ops
- [ ] Revisit Cloud Functions CORS allowlist and document how to update it
- [ ] Tighten handling of secrets (never commit keys; use Functions config / env vars)
- [ ] Add/verify ignore rules for local logs and secrets (`.env`, `serviceAccountKey.json`)

### Developer experience
- [ ] Add CI (build + test) via GitHub Actions
- [ ] Document release/versioning workflow (tags + changelog updates)

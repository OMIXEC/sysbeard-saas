<div align="center">

# ✂️ Sysbeard SaaS

**Open-source barber management & analytics suite.** Scheduling, dashboards, payments, and messaging — built with React + Firebase.

[![Version](https://img.shields.io/github/package-json/v/omixec/sysbeard-saas?label=version)](package.json)
[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-10.x-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Stripe](https://img.shields.io/badge/Stripe-Payments-635BFF?logo=stripe&logoColor=white)](https://stripe.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[Live Demo](https://sysbeard.com) · [Report Bug](https://github.com/omixec/sysbeard-saas/issues) · [Request Feature](https://github.com/omixec/sysbeard-saas/issues)

</div>

## 📌 Overview

Sysbeard is a full-stack SaaS platform designed to modernize barbershop operations. It goes beyond bookings with business intelligence, automated workflows, and a premium client experience.

## ✨ Features

- **Smart scheduling:** multi-barber support, slotting, and buffers.
- **Analytics dashboards:** revenue tracking, KPIs, and performance insights.
- **Stripe payments:** deposits, full payments, and tips.
- **Messaging & notifications:** in-app messaging and email automation.
- **Themes & i18n:** DaisyUI themes + multi-language support (incl. RTL).

## 📚 Project docs

- `CHANGELOG.md` — notable changes + roadmap (including upcoming work).

## 🖼️ Screenshots

<details>
  <summary>Open screenshots</summary>

  <div align="center">

  ### 📊 Business Intelligence Dashboard

  <img src="docs/screenshots/bb-analytics.png" width="850" alt="Sysbeard analytics dashboard" />

  ### 🗓️ Management Views

  <table>
    <tr>
      <td width="50%"><img src="docs/screenshots/bb-calendar-month.png" alt="Calendar month view" /><br/><b>Monthly Overview</b></td>
      <td width="50%"><img src="docs/screenshots/bb-calendar-day.png" alt="Calendar day view" /><br/><b>Daily Breakdown</b></td>
    </tr>
    <tr>
      <td align="center"><img src="docs/screenshots/bb-bookings-table.png" width="400" alt="Bookings table view" /><br/><b>Detailed Booking Table</b></td>
      <td align="center"><img src="docs/screenshots/bb-booking-cards.png" width="400" alt="Bookings card view" /><br/><b>Card-based Management</b></td>
    </tr>
  </table>

  ### 💬 Communication & UI

  <table>
    <tr>
      <td align="center"><img src="docs/screenshots/bb-barber-chat.png" width="400" alt="Client messaging" /><br/><b>Client Messaging</b></td>
      <td align="center"><img src="docs/screenshots/bb-booking-dark.png" width="400" alt="Luxury dark theme" /><br/><b>Luxury Dark Theme</b></td>
    </tr>
  </table>

  </div>
</details>

## 🧱 Tech Stack

| Layer | Technologies |
| --- | --- |
| **Frontend** | React, TailwindCSS, DaisyUI, Framer Motion |
| **State** | Zustand |
| **Backend** | Firebase Cloud Functions (Node.js) |
| **Database** | Cloud Firestore |
| **Payments** | Stripe |
| **Charts** | Recharts, Tremor |

## 🚀 Getting Started

### Prerequisites

- Node.js `>= 18` (frontend) and Node.js `20` (functions)
- Firebase project (Firestore + Auth) and Firebase CLI (`firebase`)
- Stripe account (optional for local UI-only work)
- Mailgun account (optional, used for email delivery via functions)

### Install

```bash
git clone https://github.com/omixec/sysbeard-saas.git
cd sysbeard-saas

npm install
npm --prefix functions install
```

### Environment variables

Copy and edit:

```bash
cp .env.example .env
```

Common variables used by the frontend:

```bash
REACT_APP_FIREBASE_API_KEY=your_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=your_project
REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=123456789
REACT_APP_FIREBASE_APP_ID=your_app_id
REACT_APP_FIREBASE_MEASUREMENT_ID=your_measurement_id_optional

REACT_APP_STRIPE_PUBLISHABLE_KEY=pk_test_xxx
REACT_APP_CLOUD_FUNCTIONS_URL=https://us-central1-your_project.cloudfunctions.net

# Optional (only needed for some screens)
REACT_APP_GOOGLE_MAPS_API_KEY=your_maps_key
REACT_APP_GOOGLE_CLIENT_ID=your_google_oauth_client_id
```

### Configure Mailgun (Cloud Functions)

```bash
firebase functions:config:set mailgun.key="your_key" mailgun.domain="your_domain"
```

If you deploy to a different domain, update the CORS allowlist in `functions/index.js`.

### Run locally

Frontend:

```bash
npm start
```

Functions emulator (separate terminal):

```bash
npm --prefix functions run serve
```

## 🌱 Demo data (optional)

Sysbeard includes a demo data seeding system for testing and screenshots.

1. Download `serviceAccountKey.json` from Firebase Console → Project Settings → Service Accounts
2. Put it in the project root (never commit it)
3. Run:

```bash
npm run seed        # Populate Firestore with demo data
npm run seed:clean  # Remove demo data
```

Demo accounts created by the seed script:

| Role | Email | Password |
| --- | --- | --- |
| Shop Owner | `demo-owner@barbersbuddies.com` | `DemoOwner2026!` |
| Customer | `demo-customer@barbersbuddies.com` | `DemoCustomer2026!` |

## 📦 Deployment

Frontend (Firebase Hosting):

```bash
npm run build
firebase deploy --only hosting
```

Cloud Functions:

```bash
npm --prefix functions run deploy
```

Firestore rules:

```bash
firebase deploy --only firestore:rules
```

## 🎨 UI/UX roadmap (in progress)

This section is a living checklist for upcoming UX + UI improvements.

### Phase 1 — Foundations

- [ ] Define a small set of design tokens (spacing, typography, radii) and apply across core components
- [ ] Standardize form inputs, buttons, and modal patterns (focus states + validation)
- [ ] Improve dark theme contrast and readability (WCAG-focused pass)
- [ ] Add consistent empty states and loading skeletons for data-heavy screens

### Phase 2 — Core flows

- [ ] Booking flow polish: clearer steps, better time-slot selection, and inline validation
- [ ] Dashboard IA cleanup: hierarchy, filters, and “at a glance” KPIs
- [ ] Messaging UX: unread states, faster thread navigation, better composer ergonomics
- [ ] Settings re-org: shop settings vs account settings, clearer defaults

### Phase 3 — Accessibility + responsiveness

- [ ] Keyboard navigation pass (modals, menus, tables) + visible focus rings
- [ ] RTL regression pass (Arabic) and layout consistency across breakpoints
- [ ] Mobile/tablet improvements for calendar + booking management views
- [ ] Performance polish for long lists (virtualization where needed)

## 🤝 Contributing

1. Fork the repo
2. Create your branch: `git checkout -b feature/awesome-feature`
3. Commit changes: `git commit -m "Add awesome feature"`
4. Push: `git push origin feature/awesome-feature`
5. Open a Pull Request

## 📄 License

MIT — see `LICENSE`.

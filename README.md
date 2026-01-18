<div align="center">

# ✂️ Sysbeard SaaS

### The Ultimate Open-Source Barber Management & Analytics Suite

**The professional command center for barbershops. Scalable, data-driven, and built for growth.**

[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/omixec/sysbeard-saas/releases)
[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![Firebase](https://img.shields.io/badge/Firebase-10.12-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Stripe](https://img.shields.io/badge/Stripe-Payments-635BFF?logo=stripe&logoColor=white)](https://stripe.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[Live Demo](https://sysbeard.com) · [Report Bug](https://github.com/omixec/sysbeard-saas/issues) · [Request Feature](https://github.com/omixec/sysbeard-saas/issues)

</div>

---

## 📖 About Sysbeard

**Sysbeard** is a high-performance SaaS platform designed to transform barbershop operations. It moves beyond simple booking by providing shop owners with deep business intelligence, automated workflows, and a premium customer experience.

By combining the "System" with the "Beard," we provide an all-in-one ecosystem for appointment scheduling, financial tracking, and staff management—allowing barbers to focus on their craft while the software handles the business.

---

## 📸 visual Tour

<div align="center">

### 📊 Business Intelligence Dashboard
<img src="docs/screenshots/bb-analytics.png" width="850" alt="Sysbeard Analytics Dashboard"/>
<p><i>Monitor your growth with real-time revenue charts, booking velocity, and performance KPIs.</i></p>

### 🗓️ Management Views
<table>
  <tr>
    <td width="50%"><img src="docs/screenshots/bb-calendar-month.png" alt="Month View"/><br/><b>Monthly Overview</b></td>
    <td width="50%"><img src="docs/screenshots/bb-calendar-day.png" alt="Day View"/><br/><b>Daily Breakdown</b></td>
  </tr>
  <tr>
    <td align="center"><img src="docs/screenshots/bb-bookings-table.png" width="400" alt="Table View"/><br/><b>Detailed Booking Table</b></td>
    <td align="center"><img src="docs/screenshots/bb-booking-cards.png" width="400" alt="Card View"/><br/><b>Card-based Management</b></td>
  </tr>
</table>

### 💬 Communication & UI
<table>
  <tr>
    <td align="center"><img src="docs/screenshots/bb-barber-chat.png" width="400" alt="Chat"/><br/><b>Client Messaging</b></td>
    <td align="center"><img src="docs/screenshots/bb-booking-dark.png" width="400" alt="Dark Mode"/><br/><b>Luxury Dark Theme</b></td>
  </tr>
</table>

</div>

---

## ⚡ Key Features

* **Smart Scheduling:** Multi-barber support with intelligent slotting and buffer times.
* **Deep Analytics:** Revenue tracking, customer retention rates, and peak-hour heatmaps.
* **Stripe Integrated:** Handle secure deposits, full payments, and tips effortlessly.
* **Multilingual:** Full support for English, German, Turkish, and Arabic (RTL).
* **Staff Performance:** Individual barber profiles with rating systems and commission tracking.
* **Omnichannel Notifications:** Email and in-app alerts powered by Mailgun and Firebase.

---

## 🛠️ Technical Stack

| Layer | Technologies |
| :--- | :--- |
| **Frontend** | React 18, TailwindCSS, Framer Motion, DaisyUI |
| **Backend** | Firebase Cloud Functions (Node.js) |
| **Database** | Cloud Firestore |
| **State** | Zustand |
| **Payments** | Stripe API |
| **Charts** | Recharts & Tremor |

---

## 🚀 Installation & Setup

### 1. Clone & Install
```bash
git clone [https://github.com/omixec/sysbeard-saas.git](https://github.com/omixec/sysbeard-saas.git)
cd sysbeard-saas
npm install
cd functions && npm install && cd ..




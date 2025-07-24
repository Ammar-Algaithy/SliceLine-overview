<p align="center">
  <img src="./assets/logo-sliceline.svg" alt="SliceLine Logo" width="180">
</p>

<h1 align="center">SliceLine 🍕 — Self‑Service Deli & Kiosk Ordering Platform</h1>

<p align="center">
  Touch‑first ordering · Real‑time kitchen display · Cash & card checkout · Admin dashboard
</p>


---

## 📸 Preview

| Kiosk Home | Item Details & Extras | Cart Overlay | Admin Orders Page |
|------------|----------------------|--------------|-------------------|
| ![Home](./assets/screenshots/kiosk-home.png) | ![Menu](./assets/SliceLine_MenuPage.png) | ![Cart](./assets/screenshots/cart.png) | ![Orders](./assets/screenshots/admin-orders.png) |

More screenshots & a short demo GIF live in [`docs/demo`](docs/demo).

---

## ✨ Key Features

- **Full‑screen kiosk UI** with large tap targets, hero slider, animated category bubbles, and horizontal “Popular” carousel.  
- **Customizable orders**: ingredient toggles, extra add‑ons, dynamic price recalculation.  
- **Smooth cart flow**: overlay panel, quantity controls, cash or card checkout, animated confirmation modals.  
- **Cash‑order staging**: unconfirmed cash orders stored in a temp table for cashier approval.  
- **Kitchen & cashier dashboards** with tabbed order boards (`Pending → Preparing → Ready`).  
- **Admin console** for products, clients, multi‑supplier pricing, and notifications.  
- **Modern stack**: React 19 · TypeScript · Redux Toolkit · Tailwind CSS · Framer Motion · ASP.NET Core 8 · EF Core · SQLite / SQL Server.

---

## 🛠 Tech Stack

| Layer        | Tech                                                                      |
|--------------|---------------------------------------------------------------------------|
| **Frontend** | React 19, TypeScript, Redux Toolkit, Tailwind CSS, Framer Motion, Axios   |
| **Backend**  | ASP.NET Core 8 Web API, Entity Framework Core, Microsoft Identity         |
| **Database** | SQLite (dev) / SQL Server (prod)                                          |
| **Auth**     | JWT bearer tokens with role‑based policies                                |
| **Dev Ops**  | GitHub Actions CI, Docker Compose (optional), Nginx reverse proxy         |

---

## 🗺 Architecture

![Architecture diagram](./assets/diagrams/architecture.svg)

1. **Kiosk & mobile clients** call the ASP.NET Core API.  
2. **TempCashOrder** flow intercepts cash checkouts before conversion to permanent orders.  
3. **Admin SPA** shares the same API and Auth server.  
4. Events are logged centrally via an `AppLog` entity for audit and troubleshooting.

---

## 🚀 Getting Started

This repository is an **overview only**.  
The full source code lives in a private repo. To request access, email **ammar@neowasl.com**.

---

## 📈 Roadmap

- [x] Kiosk ordering MVP  
- [x] Cash‑order cashier workflow  
- [x] Admin panels (products, clients, orders, notifications)  
- [ ] Real‑time WebSocket updates for kitchen displays  
- [ ] Multi‑tenant SaaS (per‑deli branding & isolation)  
- [ ] Reporting & analytics (sales heatmaps, ingredient usage)  
- [ ] Internationalization (Arabic & Spanish)

---

## 🙌 Contributing

Have design feedback or feature ideas? Open an issue here or reach out:

- **Email:** ammar@neowasl.com  
- **LinkedIn:** [Ammar Algaithy](https://linkedin.com/in/your-profile)

Code contributions occur in the private SliceLine repo via pull requests.

---

## 📜 License

The content of this overview repository is released under the **MIT License**.  
Source code in the private SliceLine repository is proprietary to NeoWasl LLC.

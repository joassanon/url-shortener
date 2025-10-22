<h1 align="center">🔗 Modern URL Shortener</h1>
<p align="center">
  <strong>A fast, privacy-friendly, analytics-powered URL shortener built with Laravel + Inertia + React</strong><br/>
  <sub>🚀 Designed for performance, extensibility, and developer happiness (DX)</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Laravel-11.x-FF2D20?style=flat-square&logo=laravel&logoColor=white" />
  <img src="https://img.shields.io/badge/Inertia.js-%FCD34D?style=flat-square&logo=inertia&logoColor=black" />
  <img src="https://img.shields.io/badge/React-18.x-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/TailwindCSS-3.x-38BDF8?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" />
</p>

---

## 🧭 Table of Contents

- [✨ Features](#-features)
- [🗺️ Roadmap](#%EF%B8%8F-roadmap)
- [🧰 Tech Stack](#-tech-stack)
- [🏗️ Project Structure](#%EF%B8%8F-project-structure)
- [🧪 Setup](#-setup)
- [🚀 Deployment](#-deployment)
- [🤝 Contributing](#-contributing)
- [🧾 License](#-license)

---

## ✨ Features

✅ Modern full-stack stack: Laravel 11 + Inertia + React + Vite  
✅ Fast redirects (Redis-cached)  
✅ Analytics dashboard with real-time updates  
✅ Custom aliases, password protection, and link expiration  
✅ Branded domains & API integration  
✅ QR code generation and CSV bulk import  
✅ Modern dashboard UI with dark mode  
✅ Built-in DX features: hot reload, linting, type safety

---

## 🗺️ Roadmap

### 🧩 Core Features

- [x] Shorten long URLs with unique hash/slugs (`hashids/hashids`)
- [x] Custom aliases (`/my-brand-link`)
- [ ] Password-protected links
- [ ] Expiration (date / click-based)
- [x] QR code generation (`simple-qrcode`)
- [ ] Bulk CSV import
- [x] API endpoint (Laravel Sanctum)
- [ ] Branded custom domains (CNAME)

---

### 📊 Analytics

- [x] Click counter + timestamp
- [ ] Device, OS, Browser (`ua-parser-js`)
- [ ] Country / City tracking (`stevebauman/location`)
- [ ] UTM parameter tracking
- [ ] Real-time analytics (`laravel-websockets` or Pusher)
- [ ] Graphs with `recharts`

---

### 🔐 Authentication

- [x] Laravel Breeze (Inertia stack)
- [ ] Team accounts (Jetstream Teams)
- [x] Sanctum API tokens
- [ ] Rate limiting + spam protection (`spatie/laravel-honeypot`)
- [ ] Social logins (Google, GitHub)

---

### 💎 UI/UX

- [x] Tailwind + shadcn/ui components
- [x] Dark mode toggle (`next-themes` or custom)
- [x] Copy to clipboard (`navigator.clipboard.writeText()`)
- [x] Toast notifications (`react-hot-toast` or `sonner`)
- [ ] Table filtering + sorting (`@tanstack/react-table`)
- [ ] Data fetching + caching (`@tanstack/react-query`)
- [ ] CSV drag & drop (`react-dropzone`)
- [ ] Smooth transitions (`framer-motion`)

---

### ⚡ Performance

- [x] Redis cache for redirects
- [x] Queues for analytics and QR generation
- [ ] Horizon dashboard for queue monitoring
- [ ] Edge/CDN redirect (Cloudflare Workers, Vercel Edge)
- [x] Docker-based local environment
- [ ] CI/CD with GitHub Actions

---

### 🌐 Sharing & Marketing

- [ ] OG meta customization
- [ ] Link preview (`embed/embed`)
- [ ] Custom analytics pixel
- [ ] Public profile / analytics sharing
- [ ] Email summaries (weekly reports)

---

### 🧠 Bonus / Future

- [ ] AI-generated link titles (OpenAI API)
- [ ] Chrome/Edge extension for quick shorten
- [ ] Zapier / Make integration
- [ ] Admin panel (`filamentphp/filament` or Laravel Nova)
- [ ] Subscription billing (Stripe via `laravel/cashier`)

---

## 🧰 Tech Stack

| Layer            | Technology                     |
| ---------------- | ------------------------------ |
| Backend          | **Laravel 11**, PHP 8.3        |
| Frontend         | **React 18**, Inertia.js, Vite |
| UI               | **Tailwind CSS 3**, shadcn/ui  |
| Database         | MySQL / PostgreSQL             |
| Caching & Queues | Redis                          |
| Realtime         | Laravel WebSockets / Pusher    |
| Charts           | Recharts / Chart.js            |
| Authentication   | Laravel Breeze + Sanctum       |
| Deployment       | Forge / Vapor / Ploi / Railway |

---

## 🏗️ Project Structure

```bash
project-root/
├── app/
│   ├── Models/
│   ├── Http/Controllers/
│   ├── Services/      # QR, Analytics, etc.
│   └── Jobs/
├── resources/
│   └── js/
│       ├── Pages/
│       ├── Components/
│       ├── Hooks/
│       └── api/
├── routes/
│   ├── web.php
│   ├── api.php
│   └── inertia.php
└── database/
    ├── migrations/
    └── seeders/
```

---

## 🧪 Setup

# 1. Clone the repo

`git clone https://github.com/yourname/url-shortener.git`
`cd url-shortener`

# 2. Install dependencies

`composer install`
`npm install`

# 3. Setup .env

`cp .env.example .env`
`php artisan key:generate`

# 4. Run migrations & seed data

`php artisan migrate --seed`

# 5. Start dev servers

`php artisan serve`
`npm run dev`

---

## 🚀 Deployment

<ul>
<li>
Backend: Laravel Forge / Vapor / Ploi / Railway
</li>
<li>
Frontend: Served via Inertia (no separate deploy needed)
</li>
<li>
Cache/Queue: Redis
</li>
<li>
DNS/CDN: Cloudflare (for edge redirects)
</li>
<li>
CI/CD: GitHub Actions for test + deploy
</li>
</ul>

---

## 🧑‍💻 Developer Experience (DX)

<ul>
<li>
🔥 Hot reload with Vite + Inertia
</li>
<li>
🧹 Code formatting via Prettier, ESLint, and Laravel Pint
</li>
<li>
🧱 Type safety with TypeScript
</li>
<li>
🔒 API validation with Zod
</li>
<li>
🧪 Environment validation with laravel-env-sync
</li>
<li>
🧰 Seeders & factories for mock data
</li>
<li>
</ul>

---

## 🤝 Contributing

Pull requests, issues, and ideas are welcome!
If you want to suggest a new feature, please open an issue describing it clearly.

---

## 🧾 License

MIT License — feel free to use, remix, and build on top of this project.
© Joas Sanon
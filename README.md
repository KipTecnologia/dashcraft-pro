# 📊 DashCraft Pro v2.0 - Enterprise SaaS Admin & Analytics

[![Next.js 15](https://img.shields.io/badge/Next.js-15.0_App_Router-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-Strict-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Prisma ORM](https://img.shields.io/badge/Prisma-ORM-2D3748?style=for-the-badge&logo=prisma)](https://prisma.io)
[![Radix UI](https://img.shields.io/badge/Radix_UI-Mantine_Design_Tokens-161618?style=for-the-badge&logo=radix-ui)](https://www.radix-ui.com/)
[![Stripe](https://img.shields.io/badge/Stripe-SaaS_Billing_&_Webhooks-635BFF?style=for-the-badge&logo=stripe)](https://stripe.com)
[![Bilingual i18n](https://img.shields.io/badge/i18n-English_%26_Português-10B981?style=for-the-badge)](https://kiptecnologia.github.io/dashcraft-pro/)
[![By Kip Tecnologia](https://img.shields.io/badge/By-Kip_Tecnologia-059669?style=for-the-badge)](https://github.com/KipTecnologia)
[![Live Demo](https://img.shields.io/badge/Live-Demo_Ready-emerald?style=for-the-badge&logo=googlechrome)](https://kiptecnologia.github.io/dashcraft-pro/)

> **English**: Production-ready **Enterprise B2B SaaS Admin & Analytics Dashboard Boilerplate**. Built with **Next.js 15 App Router**, **React 19**, **TypeScript**, **Mantine / Radix UI design tokens**, **Prisma ORM (RBAC, Audit Logs, Memberships)**, and **Turnkey Stripe SaaS Subscriptions**. Default clean corporate light aesthetic (zero AI-cliché dark neon).  
> **Português**: Painel Administrativo Executivo e Boilerplate Micro-SaaS completo para aplicações B2B. Desenvolvido com **Next.js 15**, **TypeScript**, **tokens Radix/Mantine**, **Prisma ORM (RBAC)** e **Stripe**. Criado e mantido por **[Kip Tecnologia](https://github.com/KipTecnologia)**.

---

## ⚡ Live Interactive Demo (Bilingual EN / PT)

Experience the live executive dashboard with 1-click English 🇺🇸 / Portuguese 🇧🇷 toggle:  
👉 **[https://kiptecnologia.github.io/dashcraft-pro/](https://kiptecnologia.github.io/dashcraft-pro/)**

![DashCraft Pro Preview](./public/demo_preview.gif)

- **🏛️ Refined Enterprise Aesthetic**: Light mode as primary, high-trust corporate design inspired by Linear, Mantine, and Radix. Also includes a seamless Carbon Slate dark mode.
- **📈 Interactive Revenue Analytics**: Real-time trajectory charts with variable ranges (7D, 30D, 90D, 12M).
- **🛡️ Granular RBAC Team Table**: Role filtering (Owner, Admin, Manager, Developer, Billing) and status filters (Active, Trial, Past Due, Canceled).
- **⚡ Instant CSV Export**: Native browser-based data export without server latency.
- **⌨️ Command Palette (`⌘K` / `Ctrl+K`)**: Rapid navigation and shortcut modal.
- **💳 Turnkey Stripe SaaS Monetization**: Integrated checkout flows, plan tiers ($49 Starter, $149 Pro, $499 Enterprise), and automated webhooks.

---

## 🏗️ Production Micro-SaaS Architecture

```
dashcraft-pro/
├── prisma/
│   └── schema.prisma                # User, Workspace, Membership, Subscription, Invoice, AuditLog
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── analytics/
│   │   │   │   └── metrics/route.ts # Aggregated revenue & MRR trajectory API
│   │   │   ├── users/
│   │   │   │   └── route.ts         # User management, filtering & RBAC assignment
│   │   │   └── stripe/
│   │   │       ├── checkout/route.ts# Stripe Checkout session creator
│   │   │       └── webhook/route.ts # Subscription events, renewals & cancellations
│   │   ├── globals.css              # Custom Radix scrollbars, design variables
│   │   ├── layout.tsx               # Root layout & Metadata
│   │   └── page.tsx                 # Full interactive dashboard & analytics suite
│   ├── lib/
│   │   ├── db.ts                    # Prisma client singleton
│   │   └── stripe.ts                # Stripe SDK & SaaS pricing tiers
│   └── types/
│       └── dashboard.ts             # TypeScript definitions for metrics, roles & users
├── .env.example                     # Preconfigured environment templates
├── package.json
└── README.md
```

---

## 🚀 Quick Start Guide (English)

### 1. Installation
```bash
git clone https://github.com/KipTecnologia/dashcraft-pro.git
cd dashcraft-pro
npm install
```

### 2. Configure Environment Variables
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Key configurations:
- `DATABASE_URL`: Connection string for SQLite or PostgreSQL (Supabase / Neon).
- `NEXTAUTH_SECRET`: Secret key for authentication sessions.
- `STRIPE_SECRET_KEY`: Stripe API secret for SaaS checkout and billing portal.

### 3. Initialize Database & Run
```bash
npx prisma db push
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) to view your dashboard.

---

## 🇧🇷 Guia de Início Rápido (Português)

### 1. Instalação e Execução
```bash
git clone https://github.com/KipTecnologia/dashcraft-pro.git
cd dashcraft-pro
npm install
cp .env.example .env
npx prisma db push
npm run dev
```

### 2. Configurar Variáveis de Ambiente
Preencha as chaves do Stripe e do Banco de Dados no arquivo `.env`. A aplicação suporta SQLite para desenvolvimento rápido ou PostgreSQL / Supabase para produção em grande escala.

---

## 🏢 About Kip Tecnologia

**DashCraft Pro** is engineered and maintained by **Kip Tecnologia**.

- **Website**: [kiptecnologia.com.br](https://kiptecnologia.com.br)
- **GitHub**: [github.com/KipTecnologia](https://github.com/KipTecnologia)
- **Support**: `contato@kiptecnologia.com.br`

---

## 💎 Commercial Licensing vs. Public Demo

| Feature / Asset | Public Interactive Demo (Free) | Commercial License & Full Boilerplate (Paid) |
| :--- | :---: | :---: |
| **Interactive SaaS Analytics Dashboard** | ✅ Free Access | ✅ Included |
| **Bilingual Switcher (EN / PT)** | ✅ Included | ✅ Included |
| **CSV Client Export & Filtering** | ✅ Included | ✅ Included |
| **Next.js 15 App Router Full Source Code** | ❌ (Commercial) | ✅ **100% Unlocked** |
| **Prisma ORM (RBAC, Audit Logs, Invoices)** | ❌ (Commercial) | ✅ **Production Models** |
| **API Endpoints (Metrics, Users, Subscriptions)** | ❌ (Commercial) | ✅ **Production Endpoints** |
| **Stripe Checkout & Automated Webhooks** | ❌ (Commercial) | ✅ **Turnkey Setup** |
| **Command Palette (`⌘K`) Component** | ❌ (Commercial) | ✅ **Fully Modular** |
| **100% White-Label Rights (Launch your own SaaS)** | ❌ (Evaluation only) | ✅ **Full Commercial Rights** |
| **Lifetime Updates & Priority Support** | ❌ (Evaluation only) | ✅ **Included** |

👉 **[Acquire Commercial License & Full Boilerplate on Gumroad](https://rancharia.gumroad.com)**

---

## 📄 License

This repository is governed by the **Kip Tecnologia Commercial & Evaluation License (v2.0)**. The interactive demo and public assets are available for evaluation purposes. Commercial reproduction, distribution, and SaaS operation require a valid Commercial License from Kip Tecnologia. Copyright (c) 2026 Kip Tecnologia.

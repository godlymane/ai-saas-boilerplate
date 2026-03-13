# 🚀 AI SaaS Boilerplate — Next.js 14 + OpenAI + Stripe + Auth

**The fastest way to launch an AI-powered SaaS in 2024.**

Built by autonomous AI agents grinding to hit $1M in revenue in 7 days. Production-tested. Zero fluff.

## ✨ What's Included

### Core Stack
- **Next.js 14** (App Router, Server Components, Streaming)
- **TypeScript** — fully typed, zero any's
- **Tailwind CSS** — beautiful UI out of the box
- **PostgreSQL + Prisma** — production database setup

### Authentication
- NextAuth.js v5 (beta)
- Google OAuth
- GitHub OAuth  
- Magic Link (email)
- Session management

### Payments
- Stripe Subscriptions
- 3 pricing tiers (Free / Pro $29/mo / Enterprise $99/mo)
- Webhook handling
- Customer portal
- Upgrade/downgrade flows

### AI Integration
- OpenAI GPT-4o streaming responses
- Token usage tracking
- Rate limiting by tier
- Prompt management system

### Landing Page
- Hero section with demo
- Features grid
- Pricing table
- FAQ accordion
- Testimonials
- Footer with all links
- 95+ Lighthouse score

### Dashboard
- Usage metrics
- API key management
- Billing management
- Settings page

### Developer Experience
- TypeScript strict mode
- ESLint + Prettier configured
- Husky pre-commit hooks
- GitHub Actions CI/CD
- One-click Vercel deploy
- Environment variable validation (Zod)

---

## 🛠️ Quick Start

```bash
git clone https://github.com/godlymane/ai-saas-boilerplate
cd ai-saas-boilerplate
npm install
cp .env.example .env.local
# Fill in your API keys
npx prisma db push
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and you're live.

---

## 📁 Project Structure

```
ai-saas-boilerplate/
├── app/
│   ├── (auth)/
│   │   ├── login/page.tsx
│   │   └── register/page.tsx
│   ├── (dashboard)/
│   │   ├── dashboard/page.tsx
│   │   ├── settings/page.tsx
│   │   └── billing/page.tsx
│   ├── api/
│   │   ├── auth/[...nextauth]/route.ts
│   │   ├── stripe/webhook/route.ts
│   │   └── ai/chat/route.ts
│   ├── layout.tsx
│   └── page.tsx          ← Landing page
├── components/
│   ├── landing/
│   │   ├── Hero.tsx
│   │   ├── Features.tsx
│   │   ├── Pricing.tsx
│   │   └── FAQ.tsx
│   ├── dashboard/
│   │   ├── Sidebar.tsx
│   │   └── UsageChart.tsx
│   └── ui/               ← shadcn/ui components
├── lib/
│   ├── auth.ts
│   ├── stripe.ts
│   ├── openai.ts
│   ├── rate-limit.ts
│   └── db.ts
├── prisma/
│   └── schema.prisma
├── .env.example
└── vercel.json
```

---

## 🔑 Environment Variables

```env
# App
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-here

# OAuth
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=

# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/mydb

# Stripe
STRIPE_SECRET_KEY=sk_live_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_...

# Stripe Price IDs
STRIPE_PRO_PRICE_ID=price_...
STRIPE_ENTERPRISE_PRICE_ID=price_...

# OpenAI
OPENAI_API_KEY=sk-...

# Email (Resend)
RESEND_API_KEY=re_...
FROM_EMAIL=noreply@yourdomain.com
```

---

## 💳 Pricing Tiers

| Feature | Free | Pro ($29/mo) | Enterprise ($99/mo) |
|---------|------|--------------|---------------------|
| API calls/month | 100 | 10,000 | Unlimited |
| GPT-4o access | ❌ | ✅ | ✅ |
| Custom prompts | 3 | 50 | Unlimited |
| Team members | 1 | 5 | Unlimited |
| Priority support | ❌ | ❌ | ✅ |

---

## 🚀 Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/godlymane/ai-saas-boilerplate)

---

## 📧 Support

Questions? Email: devdattareddy@gmail.com

---

*Built by autonomous AI agents. Part of the "AI agents building a $1M startup in 7 days" experiment.*  
*[Buy Me a Coffee](https://www.buymeacoffee.com/godlmane) | [Gumroad Store](https://devdattareddy.gumroad.com) | [Source Code](https://github.com/godlymane/ai-saas-boilerplate)*

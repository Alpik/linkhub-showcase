<div align="center">

![LinkHub Logo](https://raw.githubusercontent.com/Alpik/LinkHUB/main/.github/assets/logo.png)

# 🔗 LinkHub

### The Modern Link-in-Bio Platform

[![Live Demo](https://img.shields.io/badge/🌐_Live-mylinkhub.link-4CAF50?style=for-the-badge)](https://mylinkhub.link)
[![Built with React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase)](https://supabase.com/)

*A production-ready SaaS platform built from scratch - competing with Linktree*

[Features](#-features) • [Tech Stack](#-tech-stack) • [Architecture](#-architecture) • [Screenshots](#-screenshots)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Technical Challenges](#-technical-challenges-solved)
- [Security](#-security)
- [Business Model](#-business-model)
- [Installation](#-installation)
- [What I Learned](#-what-i-learned)

---

## 🎯 Overview

LinkHub is a **complete link-in-bio SaaS platform** that allows creators and influencers to centralize all their online presence in one customizable page. Think Linktree, but with more features, better UX, and built entirely from scratch.

### 🚀 Current Status
- ✅ **Live in production** with real users
- ✅ **Generating revenue** through Stripe subscriptions
- ✅ **Multi-language** support (5 languages)
- ✅ **Mobile-optimized** (60%+ mobile traffic)

### 🎥 Demo
[Watch Demo Video](your-demo-video-url) | [Try It Live](https://mylinkhub.link)

---

## ✨ Features

### 🎨 Appearance Customization
- **16+ Pre-built Themes** (Light, Dark, Gradient variations)
- **Custom Background Images** with upload
- **Avatar Upload** with automatic optimization
- **Real-time Preview** of all changes
- **Premium Themes** (exclusive to Pro users)
- **Custom Bio** with markdown support
- **Social Media Icons** with 10+ platforms

### 🔗 Link Management
- **Unlimited Links** (Pro) / 5 Links (Free)
- **Drag & Drop Reordering** for easy organization
- **Link Icons** from extensive library
- **Link Analytics** (coming soon)
- **Link Scheduling** (coming soon)
- **Link Groups** for categorization

### 🔐 Authentication & Security
- **Google OAuth** integration
- **Two-step Signup Flow** (prevents incomplete accounts)
- **Email/Password** authentication
- **Secure Session Management**
- **Profile Completion Check**
- **Anti-fraud Protection**

### 💳 Payment System
- **Stripe Checkout** integration
- **Subscription Management**
- **Webhook Handling** for events
- **Three Pricing Tiers:**
  - 🆓 **Free:** 5 links, basic themes
  - 💎 **Pro ($4.90/mo):** Unlimited links, premium features
  - 🏆 **Lifetime Founder ($49):** One-time payment, limited editions

### 🎁 Referral System
- **Unique Referral Codes** per user
- **Tier-based Rewards:**
  - 5 referrals → Free month Pro
  - 10 referrals → Lifetime Pro
- **Anti-fraud Protection** (IP tracking, time delays)
- **Referral Dashboard** with statistics

### 🌍 Internationalization
- **5 Languages:** English, French, Spanish, German, Portuguese (BR)
- **Dynamic Route Handling** (/en/, /fr/, etc.)
- **Custom Translation System** (migrated from react-i18next)
- **Language Switcher** with persistence

### 📱 User Experience
- **Fully Responsive** (mobile-first approach)
- **Progressive Web App** ready
- **Fast Loading** (<1s initial load)
- **Smooth Animations** and transitions
- **18+ Content Warning** option
- **Dark/Light Mode** compatibility

---

## 🛠️ Tech Stack

<div align="center">

### Frontend Architecture
![React](https://img.shields.io/badge/React_18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript_5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite_5-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)

### Styling & UI
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Lucide Icons](https://img.shields.io/badge/Lucide_Icons-FF6B6B?style=for-the-badge)

### Backend & Database
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Edge Functions](https://img.shields.io/badge/Deno_Edge_Functions-000000?style=for-the-badge&logo=deno&logoColor=white)

### Authentication & Security
![Google OAuth](https://img.shields.io/badge/Google_OAuth-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Supabase Auth](https://img.shields.io/badge/Supabase_Auth-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)

### Payment Processing
![Stripe](https://img.shields.io/badge/Stripe_API-008CDD?style=for-the-badge&logo=stripe&logoColor=white)
![Webhooks](https://img.shields.io/badge/Stripe_Webhooks-635BFF?style=for-the-badge&logo=stripe&logoColor=white)

### Deployment & Hosting
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Namecheap](https://img.shields.io/badge/Namecheap_DNS-FF6C2C?style=for-the-badge&logo=namecheap&logoColor=white)

</div>

### Why This Stack?

- **React + TypeScript:** Type safety and component reusability
- **Vite:** Lightning-fast dev server and optimized builds
- **Supabase:** Complete backend solution (DB + Auth + Storage + Functions)
- **Tailwind:** Rapid UI development with utility classes
- **Vercel:** Zero-config deployment with edge network
- **Stripe:** Industry-standard payment processing

---

## 🏗️ Architecture

### Database Schema
```sql
-- Users table (extends Supabase Auth)
users (
  id UUID PRIMARY KEY,
  username TEXT UNIQUE,
  display_name TEXT,
  bio TEXT,
  avatar_url TEXT,
  subscription_tier TEXT,
  referral_code TEXT UNIQUE,
  created_at TIMESTAMP
)

-- Links table
links (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  title TEXT,
  url TEXT,
  icon TEXT,
  position INTEGER,
  is_active BOOLEAN,
  created_at TIMESTAMP
)

-- Appearance customization
user_appearances (
  user_id UUID PRIMARY KEY REFERENCES users(id),
  theme TEXT,
  background_image TEXT,
  custom_css JSONB,
  updated_at TIMESTAMP
)

-- Referral tracking
referrals (
  id UUID PRIMARY KEY,
  referrer_id UUID REFERENCES users(id),
  referred_id UUID REFERENCES users(id),
  ip_address TEXT,
  reward_claimed BOOLEAN,
  created_at TIMESTAMP
)
```

### Application Structure
```
linkhub/
├── src/
│   ├── components/
│   │   ├── auth/              # Authentication components
│   │   ├── dashboard/         # User dashboard
│   │   ├── links/             # Link management
│   │   ├── appearance/        # Theme customization
│   │   ├── profile/           # Public profile view
│   │   └── ui/                # Reusable UI components
│   │
│   ├── contexts/
│   │   ├── AuthContext.tsx    # Global auth state
│   │   └── ThemeContext.tsx   # Theme management
│   │
│   ├── lib/
│   │   ├── supabase.ts        # Supabase client config
│   │   ├── stripe.ts          # Stripe utilities
│   │   └── constants.ts       # App constants
│   │
│   ├── pages/
│   │   ├── Home.tsx           # Landing page
│   │   ├── Dashboard.tsx      # User dashboard
│   │   ├── Profile.tsx        # Public profile ([username])
│   │   ├── Pricing.tsx        # Pricing page
│   │   └── Login.tsx          # Auth pages
│   │
│   ├── locales/
│   │   ├── en.json            # English translations
│   │   ├── fr.json            # French translations
│   │   └── ...                # Other languages
│   │
│   └── utils/
│       ├── validation.ts      # Form validation
│       ├── helpers.ts         # Utility functions
│       └── analytics.ts       # Analytics tracking
│
├── supabase/
│   ├── functions/
│   │   ├── stripe-webhook/    # Payment webhook handler
│   │   └── referral-check/    # Referral validation
│   │
│   └── migrations/            # Database migrations
│
├── public/
│   ├── themes/                # Theme assets
│   └── icons/                 # App icons
│
└── README.md
```

---

## 🔥 Technical Challenges Solved

### 1. **Two-Step Signup Flow**

**Problem:** Users were signing up with Google OAuth but abandoning before completing their profile, creating incomplete accounts.

**Solution:**
```typescript
// After OAuth success, redirect to profile completion
const handleGoogleAuth = async () => {
  const { data, error } = await supabase.auth.signInWithOAuth({
    provider: 'google'
  });
  
  // Check if username exists
  const { data: profile } = await supabase
    .from('users')
    .select('username')
    .eq('id', user.id)
    .single();
  
  if (!profile?.username) {
    navigate('/complete-profile'); // Force completion
  }
};
```

### 2. **Real-Time Appearance Preview**

**Problem:** Users needed to see customization changes instantly without page reload.

**Solution:**
- React Context for appearance state
- Optimistic UI updates
- Debounced auto-save to database
- Live preview component that mirrors public profile

### 3. **Anti-Fraud Referral System**

**Problem:** Users could abuse referrals with multiple accounts.

**Solution:**
```sql
-- Database-level unique constraints
CREATE UNIQUE INDEX unique_referral_per_ip 
ON referrals(referrer_id, ip_address);

-- Time-based validation (48h delay between referrals)
-- Referrer and referred can't be same IP
-- Automatic reward calculation with tier checks
```

### 4. **Secure Payment Processing**

**Problem:** Handling sensitive payment data securely.

**Solution:**
- Stripe Checkout (never touch card data)
- Webhook signature verification
- Edge Function for secure webhook processing
- Environment variable encryption
- Idempotency keys for duplicate prevention

### 5. **Multi-Language Routing Without Breaking SEO**

**Problem:** Supporting 5 languages with clean URLs and proper SEO.

**Solution:**
```typescript
// Dynamic routing: /en/dashboard, /fr/tableau-de-bord
const routes = {
  '/dashboard': {
    en: '/en/dashboard',
    fr: '/fr/tableau-de-bord',
    es: '/es/tablero',
    // ...
  }
};

// Language detection from URL + localStorage fallback
// Google indexation per language version
```

### 6. **Mobile Performance Optimization**

**Problem:** 60% of traffic is mobile, needed <1s load time.

**Challenge Solutions:**
- Lazy loading for routes and components
- Image optimization (WebP, responsive sizes)
- Code splitting by route
- Bundle size optimization (< 200KB gzipped)
- CSS purging (Tailwind unused classes removed)

---

## 🔒 Security

### Implemented Security Measures

#### 🛡️ Authentication
- OAuth 2.0 with Google
- Secure session management (JWT tokens)
- HTTP-only cookies for refresh tokens
- CSRF protection

#### 🔐 Database Security
```sql
-- Row-Level Security (RLS) policies
CREATE POLICY "Users can only read their own data"
ON users FOR SELECT
USING (auth.uid() = id);

CREATE POLICY "Users can only update their own profile"
ON users FOR UPDATE
USING (auth.uid() = id);
```

#### 🔑 API Security
- Environment variables for sensitive keys
- API rate limiting (100 req/hour on webhooks)
- CORS configuration (whitelist only)
- Webhook signature validation

#### 💳 Payment Security
- No credit card data stored
- Stripe PCI-compliant checkout
- Webhook signature verification
- Idempotency for duplicate payments

---

## 💰 Business Model

### Pricing Strategy

| Feature | Free | Pro ($4.90/mo) | Lifetime ($249) |
|---------|------|----------------|----------------|
| **Links** | 5 | ∞ Unlimited | ∞ Unlimited |
| **Themes** | Basic (10) | All (16+) | All (16+) |
| **Custom Background** | ❌ | ✅ | ✅ |
| **Premium Features** | ❌ | ✅ | ✅ |
| **Referral Rewards** | ✅ | ✅ | ✅ |
| **Priority Support** | ❌ | ✅ | ✅ |
| **Analytics** | ❌ | ✅ (soon) | ✅ (soon) |

### Revenue Streams
1. **Monthly Subscriptions** ($4.90/mo)
2. **Lifetime Plans** ($249 one-time - limited to 100 units)
3. **Future:** Custom domains, white-label solutions

### Growth Strategy
- Freemium model with clear upgrade path
- Referral program (viral growth)
- Limited Lifetime editions (scarcity marketing)
- Social media presence
- SEO optimization

---

## 📦 Installation

### Prerequisites
- Node.js 18+
- Supabase account
- Stripe account
- Vercel account (for deployment)

### Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/linkhub.git
cd linkhub

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Fill in your Supabase and Stripe keys

# Run development server
npm run dev

# Open http://localhost:8080
```

### Environment Variables
```env
# Supabase
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key

# Stripe
VITE_STRIPE_PUBLIC_KEY=your_stripe_public_key
STRIPE_SECRET_KEY=your_stripe_secret (server-only)
STRIPE_WEBHOOK_SECRET=your_webhook_secret

# App Config
VITE_APP_URL=https://mylinkhub.link
```

### Deployment
```bash
# Build for production
npm run build

# Deploy to Vercel
vercel --prod

# Set up custom domain in Vercel dashboard
# Configure DNS records in Namecheap
```

---

## 🎓 What I Learned

Building LinkHub from scratch taught me:

### 🏗️ Architecture & Design
- How to structure a scalable SaaS application
- Component-driven development with React
- State management patterns (Context API)
- Database schema design with relationships

### 💳 Payment Integration
- Stripe API and webhook handling
- Secure payment processing
- Subscription management
- Handling edge cases (failed payments, refunds)

### 🔐 Security Best Practices
- Row-Level Security implementation
- OAuth flow and session management
- API key protection
- Anti-fraud mechanisms

### 🎨 User Experience
- Mobile-first responsive design
- Real-time updates without page reloads
- Optimistic UI patterns
- Accessibility considerations

### 🚀 DevOps & Deployment
- CI/CD with Vercel
- Environment management
- Custom domain configuration
- Edge Functions deployment

### 📊 Business Skills
- Freemium model implementation
- Pricing strategy
- User analytics
- Growth hacking (referral systems)

---

## 🤝 Contributing

While this is a personal project, I'm open to:
- Bug reports
- Feature suggestions
- Code reviews
- Collaboration opportunities

Feel free to open an issue or reach out!

---

## 📫 Contact

**Béber** - Full-Stack Developer

- 🔗 [Portfolio](https://mylinkhub.link)
- 💼 [LinkedIn](https://www.linkedin.com/in/alex-mag-a20426391/)
- 📧 [Email](mylinkhubofficial@gmail.com)

---

## 📄 License

This project is proprietary and not open-source. All rights reserved.

---

<div align="center">

### ⭐ If you like this project, give it a star!

![Version](https://img.shields.io/badge/version-1.0.0-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/status-production-success?style=for-the-badge)
![Users](https://img.shields.io/badge/active_users-growing-brightgreen?style=for-the-badge)

**Built with ❤️ and lots of coffee ☕**

</div>

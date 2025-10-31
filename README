# MERICA Trader

> Local multi-vendor marketplace connecting tradespeople, contractors, and suppliers.

![License](https://img.shields.io/badge/license-Proprietary-red)
![Node](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen)
![pnpm](https://img.shields.io/badge/pnpm-%3E%3D8.0.0-yellow)

## 🚀 Quick Start

### Prerequisites

- Node.js >= 20.0.0
- pnpm >= 8.0.0
- PostgreSQL database
- Firebase CLI (for functions and emulator)

### Installation

```bash
# Clone the repository
git clone https://github.com/CPG-Ai/MERICA.git
cd MERICA

# Install dependencies
pnpm install

# Set up environment variables
cp apps/web/.env.example apps/web/.env.local
# Edit .env.local with your database and API keys

# Set up database
pnpm --filter web db:push        # Sync schema to PostgreSQL
pnpm --filter web db:seed:ref    # Seed reference tables
pnpm --filter web db:seed        # Seed mock listings

# Start development server
pnpm dev
```

Visit [http://localhost:5000](http://localhost:5000) to see the app.

## 📁 Project Structure

```
MERICA/
├── apps/
│   ├── web/          # Next.js/React + Tailwind frontend
│   └── ios/          # SwiftUI mobile app (skeleton)
├── packages/
│   ├── functions/    # Firebase Cloud Functions (TypeScript)
│   ├── shared/       # Shared TypeScript models, validators, utils
│   └── rules/        # Firestore security rules
├── config/           # Global configuration files
└── ...
```

## 🎨 Tech Stack

- **Frontend**: Next.js 14, React 18, Tailwind CSS
- **Backend**: Firebase Cloud Functions, PostgreSQL + Drizzle ORM
- **Auth**: Firebase Authentication
- **Payments**: Stripe
- **Shipping**: Shippo
- **Search**: Ready for Algolia/Meilisearch integration

## ✨ Key Features

- ✅ **PostgreSQL database** with normalized schema (categories, trades, conditions)
- ✅ **Zip code search** with real-time geocoding and distance filtering
- ✅ **75 mock listings** across 11 US cities for testing
- ✅ **Collapsible filter panel** with smooth animations
- ✅ **Multi-vendor marketplace** for trade supplies and services
- ✅ **Geographic zones** with local ranking
- ⏱️ **Auction system** for competitive bidding (in progress)
- ⏱️ **Integrated payments** via Stripe (in progress)
- ⏱️ **Shipping labels** via Shippo (in progress)
- ⏱️ **Dispute resolution** with escalation timers (in progress)

## 🛠️ Development Scripts

```bash
# Development
pnpm dev              # Start web dev server

# Database
pnpm --filter web db:push       # Sync schema to PostgreSQL
pnpm --filter web db:seed:ref   # Seed reference tables
pnpm --filter web db:seed       # Seed mock listings
pnpm --filter web db:clear      # Clear all listings

# Testing & Quality
pnpm test             # Run all tests
pnpm type-check       # Type check all packages
pnpm lint             # Lint all packages
pnpm format           # Format code with Prettier

# Build
pnpm build            # Build all packages
pnpm clean            # Clean all build artifacts
```

## 🗂️ Database Schema

### Reference Tables
- **categories**: 7 trade categories (Construction & Mechanical, etc.)
- **trades**: 83 specific trades linked to categories
- **item_types**: 3 types (Equipment, Materials, Tools)
- **conditions**: 5 conditions (New, Like New, Excellent, Good, Used)

### Main Tables
- **listings**: Marketplace listings with foreign keys to reference tables
  - Basic: id, title, description
  - Pricing: price
  - Location: location, city, state, zip_code, latitude, longitude
  - Metadata: seller, images, badges
  - Timestamps: created_at, updated_at

## 🌐 API Routes

- `GET /api/listings` - Fetch all listings with filters
- `GET /api/listings/[id]` - Get single listing details
- More routes coming soon...

## 🔧 Configuration

### Global Config (`config/global.json`)
- Feature flags (shipping sandbox, local fee waiver, boosts)
- Timeout values (disputes, auto-escalation)

### Fee Structure (`config/fees.table.v1.json`)
- Category-based percentage + fixed fees
- Fee caps per category

## 🎯 Roadmap

### ✅ Completed (MVP)
- [x] Complete monorepo structure
- [x] Branding and themes (web + iOS)
- [x] PostgreSQL integration with Drizzle ORM
- [x] Zip code search with geocoding
- [x] Distance-based filtering
- [x] Core web routes
- [x] Shared models and validators

### 🚧 In Progress
- [ ] Complete sell wizard
- [ ] User authentication (Firebase)
- [ ] Listing detail page with Q&A
- [ ] Vendor profile pages

### 📋 Planned
- [ ] Full search implementation (Algolia/Meilisearch)
- [ ] Stripe integration (checkout, webhooks)
- [ ] Shippo integration (shipping labels)
- [ ] Returns & disputes system
- [ ] Zone features (geocoding, hubs, leaderboards)
- [ ] CSV exports
- [ ] iOS app implementation
- [ ] Admin moderation tools
- [ ] Mandatory ratings system

## 🎨 Brand Assets

- **Colors**: Navy (#001F3F), Red (#B22222), Gold (#FFD700)
- **Fonts**: Bebas Neue (display), Inter (body)
- **Icon**: https://imgur.com/JcObVxn
- **Logo**: https://imgur.com/CP6pew2

## 📝 License

Proprietary - All rights reserved

## 🤝 Contributing

This is a private project. If you have access and want to contribute, please follow these guidelines:

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

## 📧 Contact

Project Link: [https://github.com/CPG-Ai/MERICA](https://github.com/CPG-Ai/MERICA)

---

Built with ❤️ for the trades community

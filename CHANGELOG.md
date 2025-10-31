# Changelog

All notable changes to the MERICA Trader project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### 🎯 Planned
- Complete sell wizard with draft autosave
- User authentication (Firebase)
- Listing detail page with Q&A panel
- Vendor profile pages (`/@username`)
- Stripe payment integration
- Shippo shipping integration
- Returns & disputes system
- Zone features and leaderboards
- CSV export functionality
- Admin moderation tools
- iOS app implementation

## [0.1.0] - 2025-10-31

### ✨ Added
- **PostgreSQL Database Integration**
  - Drizzle ORM setup with normalized schema
  - Reference tables: categories (7), trades (83), item_types (3), conditions (5)
  - Listings table with foreign key relationships
  - Database scripts: `db:push`, `db:seed:ref`, `db:seed`, `db:clear`
  - 75 diverse mock listings across 11 US cities

- **Zip Code Search**
  - Nominatim geocoding API integration (free, no API key)
  - Haversine distance calculation for accurate mileage
  - Distance filter dropdown (5, 10, 25, 50, 100 miles)
  - Real-time geocoding with loading states
  - Auto-filter and sort by distance

- **UI Improvements**
  - Collapsible filter panel with smooth animations
  - "Show Filters" button when collapsed
  - Enlarged logo (h-20)
  - Local image hosting in public folder

- **Project Setup**
  - Complete monorepo structure with pnpm workspaces
  - Next.js 14+ web application
  - SwiftUI iOS app skeleton
  - Firebase Cloud Functions stubs
  - Shared TypeScript package with models and validators
  - Firestore security rules with test suite

- **Branding & Theme**
  - Navy (#001F3F), Red (#B22222), Gold (#FFD700) color palette
  - Bebas Neue (display) and Inter (body) fonts
  - Custom Tailwind configuration
  - Brand assets hosted locally

- **Documentation**
  - Comprehensive README with setup instructions
  - PROJECT_STRUCTURE.md with complete folder tree
  - Contributing guidelines
  - GitHub issue and PR templates
  - CI/CD workflow with GitHub Actions

### 🔧 Configuration
- Global configuration file (`config/global.json`)
  - Feature flags for shipping sandbox, fee waiver, boosts
  - Timeout values for disputes and auto-escalation
- Fee structure configuration (`config/fees.table.v1.json`)
  - Category-based fees (12% tools, 10% HVAC, 5% vehicles, etc.)
  - Fixed fees and caps per category

### 🎨 Components
- ListingCard with badges (Local Pickup, Boosted, Distance)
- SearchFilters with faceted search
- BrandProvider context for theme access

### 🚀 Routes
- `/` - Home/Search grid
- `/listings/[id]` - Listing detail (basic structure)
- `/sell` - 4-step wizard (basic structure)
- `/inventory` - Private/Public tabs
- `/dashboard` - Orders, payouts, messages, disputes
- `/admin` - Moderation panel
- `/style` - Style guide (dev only)

## [0.0.1] - 2025-10-01

### 🎉 Initial Release
- Project conception and initial planning
- Repository setup on Replit (later migrated to GitHub)
- Basic monorepo structure
- Brand identity established

---

## Types of Changes
- ✨ **Added** for new features
- 🔧 **Changed** for changes in existing functionality
- 🗑️ **Deprecated** for soon-to-be removed features
- ❌ **Removed** for now removed features
- 🐛 **Fixed** for any bug fixes
- 🔒 **Security** for vulnerability fixes

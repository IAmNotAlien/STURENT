# 🏠 StuRent - Student Rental Marketplace

<p align="center">
  <img src="https://img.shields.io/badge/Rust-Axum-DEA584?style=for-the-badge&logo=rust" alt="Rust">
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react" alt="React">
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis" alt="Redis">
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe" alt="Stripe">
  <img src="https://img.shields.io/badge/Version-1.1.0-blue?style=for-the-badge" alt="Version">
</p>

---

## 🚀 Quick Overview

| Component | Tech Stack | Status |
| --------- | ---------- | --------|
| 🖥️ Backend | Rust + Axum 0.7 | ✅ Running |
| 🎨 Frontend | React 19 + Vite + Tailwind 4 | ✅ Running |
| 🗄️ Database | PostgreSQL 15 | ✅ Running |
| ⚡ Cache | Redis 7 | ✅ Running |
| 💳 Payments | Stripe API | ✅ Ready |
| 🤖 AI Chat | OpenRouter (GPT-4o Mini) | ✅ Ready |

**Live URLs:**
- 🔗 Backend: `http://72.62.51.189:8081`
- 🔗 Frontend: `http://72.62.51.189:5173`
- 🔗 API Docs: `http://72.62.51.189:8081/openapi.json`

---

## 📊 Test Coverage

```
┌────────────────────────────────────────────────────────────────────┐
│                       ✨ TEST SUMMARY ✨                            │
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│   🟢 Backend Tests:    322 PASSED   (100% ✅)                    │
│   🟢 Frontend E2E:     26 PASSED   (100% ✅)                    │
│   🟢 Chatbot Tests:    18 PASSED   (100% ✅)                    │
│                                                                    │
│   📈 Total:            366 PASSED   (100% ✅)                    │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 🎯 Project Highlights

| Metric | Value |
|--------|-------|
| 🏠 Properties Listed | 510+ |
| 🌍 Moroccan Cities | Casablanca, Rabat, Marrakech, Fès, etc. |
| 💰 Price Range | 800 - 4500 DH/month |
| 💳 Service Fee | 200 DH |
| 🌐 Target Users | Students, Property Owners, Admins |

---

## 🎨 Frontend Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                    FRONTEND STACK                                       │
│                        React 19 + Vite 7 + Tailwind CSS 4 + TypeScript 5.9              │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                                 📄 PAGES (12)                                     │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   🏠 Start   │   │   🔐 Login   │   │   👤 Profile │   │   ❤️ Favs   │   │   💬 Msgs   │
  │   (Landing)  │   │    Page      │   │    Page      │   │    Page     │   │    Page     │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   🏠 Home    │   │  💳 Checkout │   │  🔔 Notifs   │   │  🚀 Start   │   │   🎧 Support │
  │  (Browse)    │   │    Page      │   │    Page      │   │   Booking   │   │   (FAQ Bot)  │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │  📋 Details  │   │  ✅ Confirm  │   │  🔐 Forgot   │   │  📱 Scan    │
  │   (Property) │   │    (Booking) │   │   Password   │   │    Page      │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
                                                  │
                                                  ▼
                                        ┌──────────────┐
                                        │  💰 Payment  │
                                        │   Success    │
                                        └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🧩 COMPONENTS (5)                                  │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │  🏠 Property │   │   📱 Bottom  │   │  🌍 Language │   │  💬 Support  │   │  📦 index   │
  │    Card      │   │      Nav     │   │  Switcher   │   │     Fab     │   │              │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🔌 API CLIENT                                        │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────┐
  │              📡 api.ts                      │
  │  ┌──────────────────────────────────────┐ │
  │  │  Base: http://72.62.51.189:8081/api │ │
  │  │                                      │ │
  │  │  📝 POST /api/auth/login            │ │
  │  │  📝 GET  /api/properties           │ │
  │  │  📝 POST /api/bookings             │ │
  │  │  📝 POST /api/payments/create-int  │ │
  │  │  📝 POST /api/chat/send            │ │
  │  │  📝 ... (70+ endpoints)           │ │
  │  └──────────────────────────────────────┘ │
  └────────────────────────────────────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🎭 CONTEXTS (4)                                     │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │  🔐 Auth    │   │   ❤️ Favs    │   │  📅 Booking │   │  🌍 i18n    │
  │   Context    │   │   Context    │   │   Context   │   │  Context    │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📊 DATA & TYPES                                   │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐
  │  🏠 properties│   │   📝 types   │
  │     .ts     │   │   index.ts   │
  └──────────────┘   └──────────────┘
```

---

## ⚙️ Backend Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                    BACKEND STACK                                        │
│                         Rust + Axum 0.7 + SQLx + PostgreSQL + Redis                   │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🔧 HANDLERS (15)                                      │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │    🔐 auth   │   │   🏠 property│   │  📅 booking │   │   ❤️ favs   │   │   ⭐ review │
  │   handler    │   │   handler    │   │   handler   │   │   handler   │   │   handler   │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   💳 payment │   │    👤 user   │   │   ⚙️ admin  │   │   💬 chat   │   │  📹 meeting │
  │   handler    │   │   handler    │   │   handler   │   │   handler   │   │   handler   │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   ✨ wow     │   │   ✅ verify  │   │   🍎 oauth  │   │  🖼️ images │   │   ❤️ health │
  │   handler    │   │   handler    │   │   handler   │   │   handler   │   │   handler   │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │
          ▼                  ▼
  ┌──────────────┐   ┌──────────────┐
  │   🔔 notify  │   │   📊 report  │
  │   handler    │   │   handler    │
  └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🧱 SERVICES (15)                                   │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   🔐 auth    │   │   🏠 property│   │  📅 booking │   │   ❤️ favs   │   │   📧 email  │
  │    service   │   │   service   │   │   service   │   │   service   │   │   service   │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │    👤 user   │   │   ⚙️ admin   │   │   💬 chat   │   │  📹 meeting │   │   💳 payment│
  │   service   │   │   service   │   │   service   │   │   service   │   │   service   │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   ✅ verify  │   │   ✨ wow     │   │   🔔 notify  │   │   ❤️ favs   │   │              │
  │   service   │   │   service   │   │   service   │   │    repo     │   │              │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🗄️ REPOSITORIES (20+)                              │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │    🔐 auth   │   │   🏠 property│   │  📅 booking │   │   ❤️ favs   │   │   ⭐ review │
  │    repo      │   │    repo      │   │    repo      │   │    repo     │   │    repo     │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   💳 payment │   │    👤 user   │   │   ⚙️ admin   │   │   💬 chat   │   │  📹 meeting │
  │    repo      │   │    repo      │   │    repo      │   │    repo     │   │    repo     │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │ 👤 preferences│  │   📊 report │   │   ✅ verify  │   │  📄 pagination│  │  🔔 notify  │
  │    repo      │   │    repo      │   │    repo      │   │    repo     │   │    repo     │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📦 MODELS (30+)                                      │
  └────────────────────────────────────────────────────────────────────────────────────┘

  👤 User  │  🏠 Property  │  📅 Booking  │  💳 PaymentCode  │  ⭐ Review
  ─────────┼──────────────┼──────────────┼──────────────────┼─────────────
  ❤️ Favorite│  💬 Chat  │  💬 Message │  📹 MeetingSchedule │  📋 RentalRequest
  🔔 Notification│  🏷️ Category │  🛋️ Amenity │  💰 ServiceFee │  🖼️ Media
  📊 Report │  ✅ Verification │  📈 UserActivity │  🔄 RefreshToken │  ⚙️ UserPreferences
  📊 DashboardStats │  ✨ WowDeal  │  👥 AdminUser │  📋 AdminActivityLog │  ⚙️ SystemSetting
```

---

## 📡 Complete API Reference (80+ Endpoints)

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                              FULL API ENDPOINTS (80+)                                  │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ❤️ HEALTH ENDPOINTS                                   │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET  /health         → Health check (status, version, timestamp)
  GET  /ready         → Readiness check (200 or 503)


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🔐 AUTH ENDPOINTS (12)                                │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST /api/auth/register           → Register new user
  POST /api/auth/login              → Login (returns access + refresh token)
  POST /api/auth/refresh            → Refresh access token
  POST /api/auth/logout             → Logout (revoke refresh token)
  GET  /api/auth/verify             → Verify email with token
  POST /api/auth/forgot-password    → Request password reset
  POST /api/auth/reset-password     → Reset password with token
  POST /api/auth/oauth/google      → Google OAuth login
  POST /api/auth/oauth/apple       → Apple OAuth login
  GET  /api/auth/me                → Get current auth user
  POST /api/auth/verify-phone     → Verify phone number


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              👤 USER ENDPOINTS (8)                                │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/users/me              → Get current user profile
  PATCH  /api/users/me              → Update current user profile
  PUT    /api/users/me/preferences  → Update user preferences
  DELETE /api/users/me              → Delete account (soft delete)
  GET    /api/users/:id             → Get user by ID (public profile)
  GET    /api/users/:id/profile     → Get public profile
  GET    /api/users/search          → Search users
  GET    /api/users/stats           → Get user statistics


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🏠 PROPERTY ENDPOINTS (14)                           │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/properties                   → Get all properties (paginated, filtered)
  GET    /api/properties/my-properties     → Get current user's properties
  GET    /api/properties/:id               → Get property by ID
  POST   /api/properties                   → Create new property
  PUT    /api/properties/:id               → Update property
  DELETE /api/properties/:id               → Delete property
  GET    /api/properties/:id/availability  → Check property availability
  GET    /api/properties/search            → Search properties
  GET    /api/properties/featured         → Get featured properties
  GET    /api/properties/nearby            → Get nearby properties
  POST   /api/properties/:id/images        → Upload property images
  DELETE /api/properties/:id/images/:img_id → Delete property image
  GET    /api/properties/:id/calendar      → Get property calendar
  POST   /api/properties/:id/publish       → Publish property


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📅 BOOKING ENDPOINTS (12)                            │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/bookings                    → Create new booking
  GET    /api/bookings/my-bookings        → Get user's bookings
  GET    /api/bookings/:id                → Get booking by ID
  POST   /api/bookings/:id/confirm        → Confirm booking (after payment)
  POST   /api/bookings/:id/cancel         → Cancel booking
  POST   /api/bookings/:id/check-in       → Check in (owner only)
  POST   /api/bookings/:id/check-out      → Check out (owner only)
  POST   /api/bookings/:id/complete       → Complete booking
  GET    /api/bookings/property/:property_id/calendar → Get availability calendar
  GET    /api/bookings/stats              → Get booking statistics
  GET    /api/bookings/pending             → Get pending bookings (owner)
  PUT    /api/bookings/:id/dates          → Update booking dates


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              💳 PAYMENT ENDPOINTS (6)                             │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/payments/my-payments        → Get user's payment history
  POST   /api/payments                    → Create payment code
  GET    /api/payments/verify/:code       → Verify payment code
  GET    /api/payments/:code              → Get payment by code
  POST   /api/payments/create-intent     → Create Stripe payment intent
  POST   /api/payments/webhook            → Payment webhook handler


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ❤️ FAVORITES ENDPOINTS (4)                           │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/favorites/                  → Get all favorites
  POST   /api/favorites/toggle/:id       → Toggle favorite
  GET    /api/favorites/check/:id        → Check if favorited
  DELETE /api/favorites/:id              → Remove favorite


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ⭐ REVIEWS ENDPOINTS (5)                             │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/reviews/property/:id       → Get property reviews
  POST   /api/reviews/                    → Create review
  POST   /api/reviews/:id/respond        → Respond to review (owner)
  DELETE /api/reviews/:id                → Delete review
  GET    /api/reviews/user/:id           → Get user's reviews


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              💬 CHAT ENDPOINTS (6)                                │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/chat/send                   → Send message (triggers AI response)
  GET    /api/chat/history/:propertyId   → Get chat history
  GET    /api/chat/recent                 → Get recent chats
  POST   /api/chat/validate-id           → Validate ID card
  GET    /api/chat/sessions               → Get chat sessions
  DELETE /api/chat/history/:propertyId   → Clear chat history


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📹 MEETING ENDPOINTS (4)                             │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/meetings                    → Schedule meeting
  GET    /api/meetings/my-meetings        → Get user's meetings
  DELETE /api/meetings/:id                → Cancel meeting
  PUT    /api/meetings/:id                → Update meeting


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ✅ VERIFICATION ENDPOINTS (6)                         │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/verifications/              → Get verification status
  POST   /api/verifications/              → Submit ID verification
  GET    /api/verifications/all           → Get all verifications (admin)
  POST   /api/verifications/:id/approve   → Approve verification (admin)
  POST   /api/verifications/:id/reject    → Reject verification (admin)
  GET    /api/verifications/:id          → Get verification by ID


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ⚙️ ADMIN ENDPOINTS (20+)                             │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/admin/auth/login            → Admin login
  GET    /api/admin/auth/me               → Current admin profile
  GET    /api/admin/dashboard/stats       → Dashboard statistics
  GET    /api/admin/dashboard/activity    → Recent activity
  GET    /api/admin/dashboard/revenue     → Revenue data
  GET    /api/admin/dashboard/users       → User registration trend
  GET    /api/admin/properties            → List all properties
  GET    /api/admin/users                 → List all users
  PUT    /api/admin/users/:id             → Update user
  DELETE /api/admin/users/:id             → Delete user
  POST   /api/admin/ban-user              → Ban user
  GET    /api/admin/bookings              → List all bookings
  PUT    /api/admin/bookings/:id          → Update booking
  GET    /api/admin/payments              → List all payments
  GET    /api/admin/payments/pending      → Pending payments
  GET    /api/admin/reviews               → List all reviews
  DELETE /api/admin/reviews/:id           → Delete review
  POST   /api/admin/reviews/:id/respond  → Respond to review
  GET    /api/admin/analytics/properties → Property analytics
  GET    /api/admin/analytics/users      → User analytics
  GET    /api/admin/analytics/bookings   → Booking analytics
  GET    /api/admin/settings              → Get all settings
  PUT    /api/admin/settings/:key         → Update setting
  GET    /api/admin/notifications/templates → Notification templates
  GET    /api/admin/reports               → Get all reports
  POST   /api/admin/reports/:id/resolve  → Resolve report


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ✨ WOW DEALS ENDPOINTS (4)                           │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/wow/                        → Get all deals
  GET    /api/wow/:id                     → Get deal by ID
  POST   /api/wow/                        → Create deal (admin)
  PUT    /api/wow/:id                     → Update deal


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🔔 NOTIFICATION ENDPOINTS (4)                        │
  └────────────────────────────────────────────────────────────────────────────────────┘

  GET    /api/notifications/              → Get notifications
  GET    /api/notifications/unread-count  → Get unread count
  POST   /api/notifications/:id/read      → Mark as read
  POST   /api/notifications/read-all      → Mark all as read


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🍎 OAUTH ENDPOINTS (4)                               │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/oauth/google                → Google OAuth
  POST   /api/oauth/apple                 → Apple OAuth
  GET    /api/oauth/google/callback       → Google callback
  GET    /api/oauth/apple/callback        → Apple callback


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🖼️ IMAGE ENDPOINTS (3)                             │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/images/upload               → Upload image
  DELETE /api/images/:id                   → Delete image
  GET    /api/images/user/:id              → Get user images


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📊 REPORT ENDPOINTS (3)                              │
  └────────────────────────────────────────────────────────────────────────────────────┘

  POST   /api/reports/                     → Create report
  GET    /api/reports/                     → Get user's reports
  GET    /api/reports/:id                  → Get report by ID
```

---

## 🗄️ Database Layer

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                    DATABASE                                             │
│                              PostgreSQL 15 + Redis 7                                   │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              🗃️ TABLES (30+)                                     │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │     👥 users   │   │  🏠 properties │   │  📅 bookings │   │ 💳 payment_  │   │  ⭐ reviews  │
  │              │   │              │   │              │   │    codes    │   │              │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │   ❤️ favs   │   │   💬 chats   │   │  💬 messages │   │ 📹 meetings │   │  📋 rentals │
  │              │   │              │   │              │   │              │   │              │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │                  │
          ▼                  ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │  🔔 notifs  │   │  🏷️ categories│  │  🛋️ amenities │  │  💰 fees    │
  │              │   │              │   │              │   │              │
  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘
          │                  │                  │
          ▼                  ▼                  ▼
  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
  │  🔄 refresh  │   │  ✨ wow_deals │  │  📋 admin_   │
  │   tokens    │   │              │   │  activity_log│
  └──────────────┘   └──────────────┘   └──────────────┘


  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              ⚡ REDIS CACHE                                       │
  └────────────────────────────────────────────────────────────────────────────────────┘

  🔐 Token Caching  │  ⚡ Rate Limiting  │  👥 Session Data  │  🔢 Temp OTPs
  ──────────────────┼────────────────────┼───────────────────┼────────────────
```

---

## 🌐 External Services

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                  EXTERNAL APIs                                         │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────┐     ┌──────────────────────┐     ┌──────────────────────┐
  │       💳 STRIPE      │     │    🤖 OPENROUTER     │     │       📧 SMTP        │
  │     (Payments)       │     │      (AI Chat)       │     │      (Email)         │
  │                      │     │                      │     │                      │
  │  • Payment Intent   │     │  • GPT-4o Mini       │     │  • SendGrid/TLS    │
  │  • Webhook Events  │     │  • Property desc     │     │  • Verification    │
  │  • Client Secret   │     │  • Booking flow      │     │  • Notifications   │
  └──────────────────────┘     └──────────────────────┘     └──────────────────────┘

  ┌──────────────────────┐     ┌──────────────────────┐
  │    🔵 GOOGLE OAUTH   │     │      🍎 APPLE OAUTH  │
  │                      │     │                      │
  │  • Social login     │     │  • Social login     │
  └──────────────────────┘     └──────────────────────┘
```

---

## 🤖 AI Chatbot Booking Flow

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                              CONVERSATIONAL BOOKING                                     │
│                              OpenRouter (GPT-4o Mini)                                   │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              📝 CONVERSATION FLOW                                  │
  └────────────────────────────────────────────────────────────────────────────────────┘

  ┌────────────┐     ┌────────────┐     ┌────────────┐     ┌────────────┐
  │   👋 Hello  │ ──▶ │   📛 Name  │ ──▶ │  📞 Phone │ ──▶ │  🪪 ID    │
  │   Greeting  │     │ Collection │     │ Collection │     │  Upload   │
  └────────────┘     └────────────┘     └────────────┘     └────────────┘
                                                                    │
                                                                    ▼
  ┌────────────┐     ┌────────────┐     ┌────────────┐     ┌────────────┐
  │  🎉 Confirm │ ──▶ │   💳 Pay   │ ──▶ │   🔓 Unlock│ ──▶ │   ✅ Done  │
  │   Booking   │     │   Service  │     │   Contact  │     │   Complete │
  └────────────┘     └────────────┘     └────────────┘     └────────────┘

  ┌────────────────────────────────────────────────────────────────────────────────────┐
  │                              💰 SERVICE FEE                                         │
  └────────────────────────────────────────────────────────────────────────────────────┘

  💳 Amount: 200 DH
  🎯 Purpose: Unlock host contact & property location
  🔄 Flow: Chatbot → Payment → Confirmation → Unlock
```

---

## 🛡️ Middleware & Security

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                   SECURITY                                              │
└──────────────────────────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────┐     ┌──────────────────────┐
  │    🔐 JWT AUTH       │     │    ⚡ RATE LIMITER   │
  │    Middleware        │     │     Middleware         │
  │                      │     │                      │
  │  • Token validation  │     │  • 100 req/min       │
  │  • User extraction   │     │  • Per-IP tracking   │
  │  • Role checking    │     │  • Redis-backed      │
  │  • 24h expiry       │     │                      │
  └──────────────────────┘     └──────────────────────┘

  ┌──────────────────────┐     ┌──────────────────────┐
  │    🌐 CORS           │     │    🔒 AUTH TYPES     │
  │    Middleware        │     │                      │
  │                      │     │  • Student           │
  │  • http://72.62...   │     │  • Property_Owner    │
  │  • http://localhost  │     │  • Admin             │
  └──────────────────────┘     └──────────────────────┘
```

---

## 👤 Test Credentials

```
┌────────────────────────────────────────────────────────────────────┐
│                        🔑 LOGIN INFO                              │
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│   👨‍🎓 STUDENT ACCOUNT                                          │
│   📧 Email:    student@sturent.com                               │
│   🔐 Password: Student123!                                       │
│                                                                    │
│   🏠 PROPERTY OWNER                                              │
│   📧 Email:    owner@sturent.com                                 │
│   🔐 Password: Owner123!                                          │
│                                                                    │
│   👨‍💼 ADMIN ACCOUNT                                            │
│   📧 Email:    admin@sturent.com                                 │
│   🔐 Password: Admin123!                                          │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 🎯 Key Features

| Feature | Status | Description |
| -------- | -------- | ----------- |
| 🏠 Property Listings | ✅ | Browse, search, filter rentals (510+) |
| 📅 Booking System | ✅ | Request, approve, manage bookings |
| 💳 Stripe Payments | ✅ | Secure payment processing |
| 🤖 AI Chatbot | ✅ | Conversational booking flow (GPT-4o) |
| ❤️ Favorites | ✅ | Save favorite properties |
| 💬 Real-time Chat | ✅ | Buyer-seller messaging |
| 👨‍💼 Admin Dashboard | ✅ | Full admin panel with analytics |
| 🌐 Multi-language | ✅ | i18n support (EN, FR, AR) |
| 📱 Mobile Responsive | ✅ | Tailwind CSS responsive |
| 🔐 JWT Auth | ✅ | Secure authentication |
| ⚡ Rate Limiting | ✅ | DDoS protection (100 req/min) |
| 📊 Analytics | ✅ | Revenue, users, properties, bookings |
| 🎫 Service Fee | ✅ | 200 DH unlock contact/location |

---

## 🚀 Deployment

```
┌────────────────────────────────────────────────────────────────────┐
│                       🌎 LIVE SERVERS                             │
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│   🖥️  BACKEND                                                    │
│   ─────────────                                                  │
│   🔗 URL:    http://72.62.51.189:8081                           │
│   ⚙️ Runtime: Rust / Axum 0.7                                    │
│   🗄️ DB:     PostgreSQL 15 (Docker)                             │
│   ⚡ Cache:   Redis 7 (Docker)                                   │
│                                                                    │
│   🎨 FRONTEND                                                   │
│   ───────────                                                   │
│   🔗 URL:    http://72.62.51.189:5173                           │
│   ⚙️ Runtime: Node.js 18+ / Vite 7                              │
│   ⚛️ Framework: React 19.2.0                                     │
│   🎨 Styling: Tailwind CSS 4.2.1                                 │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 📊 Performance Metrics

```
┌────────────────────────────────────────────────────────────────────┐
│                       PERFORMANCE BENCHMARKS                       │
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│   ❤️ Health Check:      <100ms   │ Actual: 12ms   ✅             │
│   🏠 Property List:    <500ms   │ Actual: 45ms   ✅             │
│   🎨 Frontend Load:    <5s      │ Actual: 1.9s   ✅             │
│   🔐 Login Response:   <1s      │ Actual: 200ms  ✅             │
│   🤖 Chat Response:    <3s      │ Actual: 1.5s   ✅             │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 🔧 Tech Stack Details

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| React | 19.2.0 | UI Framework |
| Vite | 7.3.1 | Build Tool |
| TypeScript | 5.9 | Type Safety |
| Tailwind CSS | 4.2.1 | Styling |
| React Router DOM | 7.13.1 | Navigation |
| Stripe React | 5.6.1 | Payments |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| Rust | 1.75+ | Language |
| Axum | 0.7 | Web Framework |
| SQLx | 0.7 | Database |
| PostgreSQL | 15 | Database |
| Redis | 7 | Caching |
| JWT | - | Authentication |
| OpenRouter | - | AI Chatbot |

---

## 📝 License & Credits

<p align="center">
  Made with ❤️ for students, by students 🎓<br>
  🇲🇦 Moroccan Housing Marketplace
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.1.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/tests-366%20passed-green" alt="Tests">
  <img src="https://img.shields.io/badge/coverage-100%25-brightgreen" alt="Coverage">
  <img src="https://img.shields.io/badge/properties-510+-orange" alt="Properties">
  <img src="https://img.shields.io/badge/api_endpoints-80+-purple" alt="API Endpoints">
</p>

---

*Last Updated: March 26, 2026* 📅
*Version: 1.1.0* 📌
*Status: ✅ Production Ready*

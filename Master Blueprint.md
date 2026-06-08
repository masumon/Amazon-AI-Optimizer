amazon-ai-optimizer/
│
├── README.md
│   └─ Project overview, installation, deployment guide
│   └─ Technology: Markdown
│
├── LICENSE
│   └─ Project license
│
├── .gitignore
│   └─ Ignore env, cache, build files
│
├── .env.example
│   └─ Environment variable template
│
├─────────────────────────────────────────────
│ DOCUMENTATION
├─────────────────────────────────────────────
│
├── docs/
│   │
│   ├── architecture.md
│   │   └─ System architecture diagrams
│   │
│   ├── deployment.md
│   │   └─ Vercel + Render deployment steps
│   │
│   ├── amazon-sp-api.md
│   │   └─ SP-API setup instructions
│   │
│   ├── prompt-engineering.md
│   │   └─ A10 + COSMO + Rufus strategy
│   │
│   ├── database-schema.md
│   │   └─ Database design
│   │
│   └── troubleshooting.md
│       └─ Common errors and fixes
│
├─────────────────────────────────────────────
│ FRONTEND (NEXT.JS + PWA)
├─────────────────────────────────────────────
│
├── frontend/
│
│   ├── package.json
│   │   └─ Next.js dependencies
│
│   ├── next.config.js
│   │   └─ Next configuration
│
│   ├── tsconfig.json
│   │   └─ TypeScript configuration
│
│   ├── tailwind.config.ts
│   │   └─ Tailwind setup
│
│   ├── vercel.json
│   │   └─ Vercel deployment settings
│
│   ├── middleware.ts
│   │   └─ Route protection
│
│   ├─────────────────────────
│   │ APP ROUTER
│   ├─────────────────────────
│
│   ├── app/
│   │
│   │   ├── layout.tsx
│   │   │   └─ Global layout
│   │   │   └─ Technology: Next.js
│   │
│   │   ├── page.tsx
│   │   │   └─ Dashboard Home
│   │
│   │   ├── manifest.ts
│   │   │   └─ PWA Manifest
│   │
│   │   ├── globals.css
│   │   │   └─ Global CSS
│   │
│   │   ├── dashboard/
│   │   │   └─ Overview statistics
│   │
│   │   ├── generate/
│   │   │   └─ Generate listing UI
│   │
│   │   ├── publish/
│   │   │   └─ Publish listing UI
│   │
│   │   ├── listings/
│   │   │   └─ Listing management
│   │
│   │   ├── keywords/
│   │   │   └─ Keyword tools
│   │
│   │   ├── competitors/
│   │   │   └─ Competitor analysis
│   │
│   │   ├── analytics/
│   │   │   └─ Reports and charts
│   │
│   │   ├── templates/
│   │   │   └─ Prompt templates
│   │
│   │   ├── settings/
│   │   │   └─ API configuration
│   │
│   │   └── offline/
│   │       └─ PWA offline screen
│
│   ├─────────────────────────
│   │ COMPONENTS
│   ├─────────────────────────
│
│   ├── components/
│   │
│   │   ├── ProductForm.tsx
│   │   │   └─ Product input form
│   │
│   │   ├── ListingPreview.tsx
│   │   │   └─ Preview AI output
│   │
│   │   ├── PublishButton.tsx
│   │   │   └─ Publish to Amazon
│   │
│   │   ├── HistoryTable.tsx
│   │   │   └─ Listing history
│   │
│   │   ├── Navbar.tsx
│   │   ├── Sidebar.tsx
│   │   └── LoadingSpinner.tsx
│
│   ├─────────────────────────
│   │ API LAYER
│   ├─────────────────────────
│
│   ├── lib/
│   │
│   │   ├── api.ts
│   │   │   └─ FastAPI requests
│   │
│   │   ├── auth.ts
│   │   │   └─ Authentication helpers
│   │
│   │   ├── validators.ts
│   │   │   └─ Form validation
│   │
│   │   └── types.ts
│   │       └─ Shared TS types
│
│   ├── hooks/
│   │
│   │   ├── useGenerate.ts
│   │   ├── usePublish.ts
│   │   └── useHistory.ts
│
│   ├─────────────────────────
│   │ PWA FILES
│   ├─────────────────────────
│
│   ├── public/
│   │
│   │   ├── icon-192.png
│   │   │   └─ Android icon
│   │
│   │   ├── icon-512.png
│   │   │   └─ PWA icon
│   │
│   │   ├── apple-touch-icon.png
│   │   │   └─ iOS icon
│   │
│   │   ├── favicon.ico
│   │   │   └─ Browser icon
│   │
│   │   └── sw.js
│   │       └─ Service Worker
│
├─────────────────────────────────────────────
│ BACKEND (FASTAPI)
├─────────────────────────────────────────────
│
├── backend/
│
│   ├── requirements.txt
│   │   └─ Python dependencies
│
│   ├── Dockerfile
│   │   └─ Container deployment
│
│   ├── render.yaml
│   │   └─ Render configuration
│
│   ├── .env.example
│
│   ├── app/
│   │
│   ├── main.py
│   │   └─ FastAPI entry point
│
│   ├── config.py
│   │   └─ Environment settings
│
│   ├── database.py
│   │   └─ Neon connection
│
│   ├── dependencies.py
│   │   └─ Dependency injection
│
│   ├─────────────────────────
│   │ ROUTERS
│   ├─────────────────────────
│
│   ├── routers/
│   │
│   │   ├── generate.py
│   │   │   └─ Generate listing endpoint
│   │
│   │   ├── publish.py
│   │   │   └─ Publish endpoint
│   │
│   │   ├── listings.py
│   │   │   └─ Listing CRUD
│   │
│   │   ├── keywords.py
│   │   │   └─ Keyword endpoints
│   │
│   │   ├── competitors.py
│   │   │   └─ Competitor analysis
│   │
│   │   ├── analytics.py
│   │   │   └─ Dashboard analytics
│   │
│   │   ├── settings.py
│   │   │   └─ User settings
│   │
│   │   └── health.py
│   │       └─ Keep-alive endpoint
│
│   ├─────────────────────────
│   │ SERVICES
│   ├─────────────────────────
│
│   ├── services/
│   │
│   │   ├── openai_service.py
│   │   │   └─ GPT integration
│   │
│   │   ├── anthropic_service.py
│   │   │   └─ Claude integration
│   │
│   │   ├── amazon_service.py
│   │   │   └─ SP-API integration
│   │
│   │   ├── keyword_service.py
│   │   │   └─ Keyword intelligence
│   │
│   │   ├── analytics_service.py
│   │   │   └─ Analytics engine
│   │
│   │   └── publish_service.py
│   │       └─ Publish workflow
│
│   ├─────────────────────────
│   │ AI PROMPTS
│   ├─────────────────────────
│
│   ├── prompts/
│   │
│   │   ├── title.txt
│   │   ├── bullets.txt
│   │   ├── description.txt
│   │   ├── search_terms.txt
│   │   └── compliance.txt
│
│   ├─────────────────────────
│   │ DATABASE MODELS
│   ├─────────────────────────
│
│   ├── models/
│   │
│   │   ├── users.py
│   │   ├── listing_history.py
│   │   ├── publish_history.py
│   │   ├── keyword_history.py
│   │   ├── competitors.py
│   │   └── settings.py
│
│   ├─────────────────────────
│   │ SECURITY
│   ├─────────────────────────
│
│   ├── security/
│   │
│   │   ├── jwt.py
│   │   ├── password.py
│   │   └── permissions.py
│
│   ├─────────────────────────
│   │ UTILITIES
│   ├─────────────────────────
│
│   ├── utils/
│   │
│   │   ├── logger.py
│   │   ├── retry.py
│   │   └── helpers.py
│
│   └── migrations/
│       └─ Alembic migrations
│
├─────────────────────────────────────────────
│ DATABASE
├─────────────────────────────────────────────
│
├── database/
│
│   ├── schema.sql
│   │   └─ Table definitions
│
│   ├── indexes.sql
│   │   └─ Performance indexes
│
│   └── seed.sql
│       └─ Initial data
│
├─────────────────────────────────────────────
│ AUTOMATION
├─────────────────────────────────────────────
│
├── scripts/
│
│   ├── setup.ps1
│   │   └─ Windows setup
│
│   ├── setup.sh
│   │   └─ Linux setup
│
│   ├── backup.py
│   │   └─ Backup data
│
│   └── keep_alive.py
│       └─ Render anti-sleep
│
└─────────────────────────────────────────────
MAIN TECHNOLOGY STACK
─────────────────────────────────────────────

Frontend      → Next.js 15 + TypeScript + Tailwind
PWA           → Manifest + Service Worker
Backend       → FastAPI
Database      → Neon PostgreSQL
ORM           → SQLAlchemy
Migration     → Alembic
AI            → OpenAI GPT-4o / GPT-4.1
Alternative   → Claude Sonnet
Amazon        → SP-API
Hosting       → Vercel + Render
Auth          → JWT
Deployment    → Docker
CI/CD         → GitHub Actions

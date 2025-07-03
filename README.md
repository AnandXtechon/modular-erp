my-erp-app/
├── app/
│   ├── (auth)/                    # Login, register, password reset, etc.
│   ├── admin/                     # ✅ Admin-only routes
│   │   ├── layout.tsx             # Admin dashboard layout (sidebar + header)
│   │   ├── page.tsx               # Admin home (overview or stats)
│   │   ├── modules/               # 🔧 Module manager (CRUD modules)
│   │   │   └── [moduleId]/fields/ # Manage fields for a specific module
│   │   ├── users/                 # Manage app users (roles, permissions)
│   │   └── settings/              # Global ERP app settings (AI, billing, etc.)
│   ├── dashboard/                 # User-facing dashboard (non-admins)
│   │   ├── modules/               # Dynamic modules like /customers, etc.
│   │   │   └── [slug]/            # Dynamic route for user-created modules
│   │   │       ├── page.tsx       # List entries
│   │   │       └── new.tsx        # Add new entry
│   │   └── settings/              # User-specific settings (profile, theme)
│   ├── api/                       # All backend logic (see below)
│   └── layout.tsx
│   └── page.tsx
│
├── components/
│   ├── ui/                        # shadcn/ui or custom UI components
│   ├── admin/                     # Admin-specific components (e.g., module builder)
│   └── forms/                     # Form rendering engine from DB schema
│
├── lib/
│   ├── db.ts                      # Prisma client
│   ├── auth.ts                    # Auth + role check helpers
│   └── formBuilder.ts             # Converts field config → form elements
│
├── prisma/
│   ├── schema.prisma              # Includes users, modules, fields, roles
│   └── seed.ts                    # Seeds demo modules and admin user
│
├── types/
│   └── index.d.ts                 # Types for Field, Module, User, Record, etc.
│
├── public/
├── styles/
├── .env
├── next.config.js
├── tsconfig.json
└── package.json

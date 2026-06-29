# CFD Pandeyan System Information

This is a clean, scalable, and production-ready monorepo for the **CFD Pandeyan System Information** project, managed with **Turborepo** and **pnpm workspaces**.

## Technology Stack
- **Monorepo:** Turborepo
- **Package Manager:** pnpm
- **Frontend:** Next.js 15+ (App Router) + TypeScript
- **Styling:** Tailwind CSS + shadcn/ui
- **Backend:** NestJS
- **ORM:** Prisma
- **Database:** PostgreSQL
- **Validation:** Zod
- **Icons:** Lucide React
- **Animation:** Framer Motion

## Folder Structure
```
cfd-pandeyan-system-information/
├── apps/
│   ├── api/        # NestJS Backend
│   └── web/        # Next.js Frontend
├── packages/
│   ├── ui/         # Shared UI Components (Tailwind & shadcn/ui)
│   ├── utils/      # Shared Helper Utilities
│   ├── types/      # Shared TypeScript Types & Zod Schemas
│   └── config/     # Shared ESlint, Tsconfig, and Styling Configurations
├── prisma/         # Prisma Schema & Migrations
└── turbo.json      # Turborepo Configuration
```

## Getting Started

### Prerequisites
- Node.js >= 18
- pnpm >= 9
- PostgreSQL database instance running

### Installation & Run

1. Clone the repository and install dependencies:
   ```bash
   pnpm install
   ```

2. Configure environment variables:
   - Copy `apps/api/.env.example` to `apps/api/.env` and update the `DATABASE_URL` and other variables.
   - Copy `apps/web/.env.example` to `apps/web/.env` if needed.

3. Run Prisma migrations:
   ```bash
   pnpm db:push
   ```

4. Start all applications in development mode:
   ```bash
   pnpm dev
   ```

### Scripts
- `pnpm dev`: Start NestJS and Next.js in parallel with hot reloading.
- `pnpm build`: Build all workspaces and packages.
- `pnpm lint`: Lint the entire project.
- `pnpm db:generate`: Regenerate Prisma Client.
- `pnpm db:push`: Sync Prisma schema to PostgreSQL database.

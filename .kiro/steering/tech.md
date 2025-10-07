## Tech Stack

### Framework & Runtime
- Next.js 15 (App Router)
- React 19
- TypeScript 5 (strict mode enabled)
- Node.js (ES2017 target)

### UI & Styling
- Tailwind CSS 4
- **Admin**: shadcn/ui components (New York style) with Radix UI primitives
- **Client**: Custom components with lucide-react icons
- PostCSS for CSS processing

### State & Forms
- Zustand for state management (client)
- React Hook Form with Zod validation
- @hookform/resolvers for schema validation

### Additional Libraries
- **Admin**: TanStack Table, Recharts, date-fns, next-themes
- **Client**: react-toastify for notifications

### Development Tools
- ESLint with Next.js config (core-web-vitals + TypeScript)
- Turbopack for fast development builds

## Common Commands

### Development
```bash
npm run dev          # Start dev server with Turbopack (port 3000)
```

### Production
```bash
npm run build        # Create production build
npm start            # Start production server
```

### Code Quality
```bash
npm run lint         # Run ESLint checks
```

### Working with Multiple Apps
Navigate to `client/` or `admin/` directory before running commands, as each app is independent.

## Build System Notes
- Uses Turbopack for faster development builds
- Path alias `@/*` maps to `./src/*` in both apps
- Incremental TypeScript compilation enabled

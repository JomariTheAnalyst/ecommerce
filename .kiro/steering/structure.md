## Project Structure

Monorepo with two independent Next.js applications:

```
/
├── client/          # Customer-facing storefront
│   ├── src/
│   │   ├── app/         # Next.js App Router pages
│   │   ├── components/  # React components
│   │   ├── stores/      # Zustand state stores
│   │   └── types.ts     # TypeScript type definitions
│   ├── public/          # Static assets
│   └── package.json
│
└── admin/           # Admin dashboard
    ├── src/
    │   ├── app/         # Next.js App Router pages
    │   ├── components/  # React components (includes shadcn/ui)
    │   ├── hooks/       # Custom React hooks
    │   └── lib/         # Utility functions
    ├── public/          # Static assets
    ├── components.json  # shadcn/ui configuration
    └── package.json
```

## Conventions

### Import Paths
- Use `@/*` alias for imports from `src/` directory
- Example: `import { Button } from '@/components/ui/button'`

### Component Organization
- **Admin**: UI components from shadcn/ui live in `@/components/ui`
- Shared utilities in `@/lib` (admin) or co-located with components (client)
- Custom hooks in `@/hooks` (admin only)

### Styling
- Tailwind utility classes for styling
- CSS variables for theming (admin uses shadcn/ui theme system)
- Global styles in `src/app/globals.css`

### TypeScript
- Strict mode enabled
- Define types in dedicated files or co-located with components
- Use Zod schemas for runtime validation

### App Router
- Both apps use Next.js App Router (not Pages Router)
- Server Components by default
- Use `'use client'` directive when needed for client-side interactivity

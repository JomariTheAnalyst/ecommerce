# Boys at the back - Admin Dashboard

Administrative dashboard for managing products, orders, and store operations. Built with Next.js 15, React 19, TypeScript, and shadcn/ui.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v20 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn** or **pnpm**
- **Git** - [Download here](https://git-scm.com/)

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd e-commerce-ui/admin
```

### 2. Install Dependencies

```bash
npm install
```

If you encounter dependency conflicts, try:

```bash
npm install --legacy-peer-deps
```

### 3. Environment Setup

Create a `.env.local` file in the `admin` directory:

```env
# Add your environment variables here
NEXT_PUBLIC_API_URL=http://localhost:3000
```

### 4. Run Development Server

```bash
npm run dev
```

The admin dashboard will start on [http://localhost:3000](http://localhost:3000)

Open your browser and navigate to the URL above to access the admin panel.

## Available Scripts

### Development

```bash
npm run dev
```

Starts the development server with Turbopack for fast refresh and hot module replacement.

### Production Build

```bash
npm run build
```

Creates an optimized production build of the application.

### Start Production Server

```bash
npm start
```

Runs the production build. Must run `npm run build` first.

### Linting

```bash
npm run lint
```

Runs ESLint to check for code quality issues.

## Project Structure

```
admin/
├── src/
│   ├── app/              # Next.js App Router pages
│   │   ├── layout.tsx    # Root layout
│   │   ├── page.tsx      # Dashboard homepage
│   │   └── globals.css   # Global styles
│   ├── components/       # React components
│   │   ├── ui/          # shadcn/ui components
│   │   └── ...          # Custom components
│   ├── hooks/           # Custom React hooks
│   └── lib/             # Utility functions
│       └── utils.ts     # Helper utilities
├── public/              # Static assets
├── components.json      # shadcn/ui configuration
├── package.json
└── tsconfig.json
```

## Tech Stack

- **Framework**: Next.js 15 (App Router)
- **UI Library**: React 19
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4
- **Component Library**: shadcn/ui (New York style)
- **UI Primitives**: Radix UI
- **Form Handling**: React Hook Form with Zod validation
- **Tables**: TanStack Table
- **Charts**: Recharts
- **Date Handling**: date-fns
- **Theme**: next-themes (dark/light mode)
- **Icons**: Lucide React

## Key Features

- Modern admin dashboard UI with shadcn/ui
- Dark/light theme support
- Data tables with sorting, filtering, and pagination
- Interactive charts and analytics
- Form validation with Zod schemas
- Responsive design for all screen sizes
- Type-safe development with TypeScript

## Development Tips

### Path Aliases

Use the configured aliases to import from various directories:

```typescript
import { Button } from '@/components/ui/button'
import { cn } from '@/lib/utils'
import { useToast } from '@/hooks/use-toast'
```

### Adding shadcn/ui Components

To add new shadcn/ui components:

```bash
npx shadcn@latest add button
npx shadcn@latest add dialog
npx shadcn@latest add table
```

Components will be added to `src/components/ui/`

### Theme Configuration

The project uses CSS variables for theming. Modify colors in `src/app/globals.css`:

```css
:root {
  --background: 0 0% 100%;
  --foreground: 0 0% 3.9%;
  /* ... */
}
```

### Creating New Pages

Create files in the `src/app` directory:

```
src/app/dashboard/page.tsx           → /dashboard
src/app/products/page.tsx            → /products
src/app/products/[id]/edit/page.tsx  → /products/:id/edit
```

## Running Both Client and Admin

To run both applications simultaneously:

### Terminal 1 (Client)
```bash
cd client
npm run dev
```

### Terminal 2 (Admin)
```bash
cd admin
npm run dev -- -p 3001
```

The admin will run on port 3001 to avoid conflicts with the client.

## Troubleshooting

### Port Already in Use

If port 3000 is already in use, specify a different port:

```bash
npm run dev -- -p 3001
```

### Module Not Found Errors

Clear Next.js cache and reinstall:

```bash
rm -rf .next node_modules
npm install
npm run dev
```

### shadcn/ui Component Issues

Ensure `components.json` is properly configured and all dependencies are installed:

```bash
npm install @radix-ui/react-dialog @radix-ui/react-dropdown-menu
```

### TypeScript Errors

Check `tsconfig.json` path mappings and ensure all imports use the correct aliases.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

1. Create a feature branch
2. Make your changes
3. Run `npm run lint` to check for issues
4. Test your changes thoroughly
5. Submit a pull request

## License

Private - All rights reserved

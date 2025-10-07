# Boys at the back - Client (Customer Storefront)

E-commerce customer-facing application built with Next.js 15, React 19, and TypeScript.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v20 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn** or **pnpm**
- **Git** - [Download here](https://git-scm.com/)

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd e-commerce-ui/client
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

Create a `.env.local` file in the `client` directory:

```env
# Add your environment variables here
NEXT_PUBLIC_API_URL=http://localhost:3000
```

### 4. Run Development Server

```bash
npm run dev
```

The application will start on [http://localhost:3000](http://localhost:3000)

Open your browser and navigate to the URL above to see the storefront.

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
client/
├── src/
│   ├── app/              # Next.js App Router pages
│   │   ├── layout.tsx    # Root layout
│   │   ├── page.tsx      # Homepage
│   │   └── globals.css   # Global styles
│   ├── components/       # React components
│   │   ├── Navbar.tsx
│   │   ├── Footer.tsx
│   │   └── ...
│   ├── stores/          # Zustand state management
│   └── types.ts         # TypeScript type definitions
├── public/              # Static assets (images, fonts)
├── package.json
├── tsconfig.json
└── tailwind.config.ts
```

## Tech Stack

- **Framework**: Next.js 15 (App Router)
- **UI Library**: React 19
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4
- **State Management**: Zustand
- **Form Handling**: React Hook Form with Zod validation
- **Icons**: Lucide React
- **Notifications**: React Toastify

## Key Features

- Server-side rendering with Next.js App Router
- Responsive design with Tailwind CSS
- Type-safe development with TypeScript
- Form validation with Zod schemas
- Global state management with Zustand
- Optimized images with Next.js Image component

## Development Tips

### Path Aliases

Use the `@/*` alias to import from the `src` directory:

```typescript
import { Button } from '@/components/Button'
import { useCartStore } from '@/stores/cartStore'
```

### Adding New Pages

Create files in the `src/app` directory following Next.js App Router conventions:

```
src/app/products/page.tsx       → /products
src/app/products/[id]/page.tsx  → /products/:id
```

### Styling

Use Tailwind utility classes for styling:

```tsx
<div className="flex items-center gap-4 p-6 bg-white rounded-lg shadow-md">
  {/* content */}
</div>
```

## Troubleshooting

### Port Already in Use

If port 3000 is already in use, you can specify a different port:

```bash
npm run dev -- -p 3001
```

### Module Not Found Errors

Clear Next.js cache and reinstall dependencies:

```bash
rm -rf .next node_modules
npm install
npm run dev
```

### TypeScript Errors

Check your `tsconfig.json` and ensure all paths are correctly configured.

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

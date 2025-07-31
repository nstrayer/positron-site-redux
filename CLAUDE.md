# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Common Commands

### Development
- `npm run dev` - Start the development server at http://localhost:4321
- `npm run build` - Run type checking and build for production (outputs to `dist/`)
- `npm run preview` - Preview the production build locally

### Component Management
- `npx shadcn-ui@latest add [component-name]` - Add new shadcn/ui components

## Architecture

This is a **static landing page** built with Astro, using React for interactive components. The architecture follows a component-based approach with:

### Technology Stack
- **Astro** - Static site generator for optimal performance
- **React** - Used for interactive UI components via Astro's React integration
- **Tailwind CSS** - Utility-first CSS framework with custom color variables
- **shadcn/ui** - React component library built on Radix UI primitives
- **TypeScript** - Type safety across the codebase

### Key Patterns

1. **Astro Components** (`.astro` files) - Used for static page sections and layouts
   - Located in `src/components/` and `src/layouts/`
   - Can import and use React components

2. **React Components** (`.tsx` files) - Used for interactive UI elements
   - Located in `src/components/ui/`
   - Built with shadcn/ui patterns using Radix UI primitives
   - Styled with Tailwind CSS and CSS variables

3. **Styling Architecture**
   - Global styles and CSS variables in `src/styles/globals.css`
   - Tailwind configuration with custom Posit brand colors:
     - Primary: `#447099` (posit-blue)
     - Secondary: `#EE6331` (posit-orange)
   - Component-specific styles use Tailwind utilities

4. **Path Aliases**
   - `@/*` maps to `./src/*` for clean imports

## Important Configuration

- **Astro Config**: Base styles are disabled (`applyBaseStyles: false`) to use custom global styles
- **Radix UI**: Configured as SSR no-external in Vite to prevent hydration issues
- **TypeScript**: Strict mode enabled via Astro's tsconfig preset
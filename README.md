# Positron Landing Page

A modern, responsive landing page for Positron - the next-generation data science IDE built by Posit PBC.

## Tech Stack

- **Framework**: [Astro](https://astro.build/) - Static site generator
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) + [shadcn/ui](https://ui.shadcn.com/)
- **Components**: React (for interactive components)
- **Animations**: CSS animations + Framer Motion
- **Icons**: Lucide React

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or pnpm

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

3. Open [http://localhost:4321](http://localhost:4321) in your browser

### Building for Production

```bash
npm run build
```

The built site will be in the `dist/` directory.

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
/
├── public/
│   └── images/         # Static images
├── src/
│   ├── components/     # Astro and React components
│   │   └── ui/        # shadcn/ui components
│   ├── layouts/       # Page layouts
│   ├── pages/         # Route pages
│   ├── styles/        # Global styles
│   └── lib/           # Utility functions
```

## Features

- ✨ Modern, clean design with smooth animations
- 📱 Fully responsive (mobile-first approach)
- 🚀 Excellent performance (static generation)
- ♿ Accessible components (via shadcn/ui)
- 🎨 Consistent design system with Tailwind CSS
- 🌗 Dark mode ready (CSS variables configured)

## Customization

### Colors

The color scheme uses CSS variables defined in `src/styles/globals.css`. The main brand colors are:

- Primary (Posit Blue): `#447099`
- Secondary (Posit Orange): `#EE6331`
- Grays and neutrals from Tailwind

### Adding New Components

1. For UI components, use the shadcn/ui CLI:
```bash
npx shadcn-ui@latest add [component-name]
```

2. For page sections, create new `.astro` files in `src/components/`

### Content Updates

- Hero text: Edit `src/components/Hero.astro`
- Features: Update the `features` array in `src/components/Features.astro`
- Footer links: Modify `src/pages/index.astro`

## License

This landing page follows the same licensing as Positron - see the main Positron repository for details.
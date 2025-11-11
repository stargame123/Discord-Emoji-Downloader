# Replit Setup Guide

This project is configured to run on Replit. Follow these steps to get started.

## Prerequisites

- Node.js 18.16.1 or higher
- npm or yarn package manager

## Quick Start

1. **Clone or Fork this repository** on Replit

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```

4. The application will open automatically in a new tab at `http://localhost:3000`

## Available Commands

- `npm run dev` - Start development server with Vite
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Environment Variables

Configure these in your `.env.local` file:

```
VITE_API_URL=http://localhost:5000
```

## Troubleshooting

- **Port already in use**: The dev server runs on port 3000 by default
- **Module not found**: Run `npm install` again to ensure all dependencies are installed
- **Build errors**: Clear node_modules and reinstall with `npm install`

## Resources

- [Vite Documentation](https://vitejs.dev/)
- [React Documentation](https://react.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [shadcn/ui](https://ui.shadcn.com/)

## Support

For issues or questions, refer to the main README.md file.

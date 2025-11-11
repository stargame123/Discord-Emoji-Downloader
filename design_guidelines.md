# Design Guidelines

## Project Overview

Discord Emoji Downloader is a modern web application for bulk downloading emojis from Discord servers with an intuitive interface and efficient server management.

## Color Palette

### Primary Colors
- **Discord Blue**: #5865F2 (Primary action color)
- **Success Green**: #57F287 (Success states)
- **Warning Yellow**: #FED93D (Alerts and warnings)
- **Error Red**: #ED4245 (Error states)
- **Neutral Gray**: #313338 (Text and backgrounds)

### Tailwind Configuration
Use the configured color system in `tailwind.config.ts` for consistency.

## Typography

### Font Stack
- Primary: Inter (via @font-face or cdn)
- Fallback: System fonts from defaultTheme

### Font Sizes
- H1: 2.5rem (40px) - Page titles
- H2: 2rem (32px) - Section headers
- H3: 1.5rem (24px) - Subsection headers
- Body: 1rem (16px) - Regular text
- Small: 0.875rem (14px) - Secondary text
- Tiny: 0.75rem (12px) - Captions

## Component Guidelines

### shadcn/ui Components
Use shadcn/ui components for consistency:
- Buttons, Inputs, Forms
- Dialogs, Dropdowns, Menus
- Cards, Tables, Lists
- Notifications/Toasts

### Dark Mode
- Fully supported via Tailwind dark mode (class strategy)
- Toggle in settings for user preference
- Always provide light/dark variants

## Layout Principles

1. **Responsive Design**: Mobile-first approach
2. **Grid System**: 12-column grid for consistency
3. **Spacing**: Use 4px base unit (4px, 8px, 16px, 24px, 32px...)
4. **Z-index**: Manage layers (modals > dropdowns > content)

## Interaction Patterns

### Buttons
- Primary: Main actions (download, upload)
- Secondary: Alternative actions
- Tertiary: Less important actions
- Include loading states with spinners

### Forms
- Label above input
- Error messages below field
- Inline validation feedback
- Clear focus states

### Animations
- Duration: 200-300ms for most interactions
- Easing: ease-out for appearing, ease-in for disappearing
- Never exceed 500ms for loading states

## Accessibility Requirements

- WCAG 2.1 Level AA compliance
- Keyboard navigation support
- ARIA labels for screen readers
- Color contrast ratio: 4.5:1 for text
- Focus indicators visible on all interactive elements

## File Structure

```
src/
├── components/
│   ├── ui/          # shadcn/ui components
│   ├── forms/       # Form components
│   └── layout/      # Layout components
├── lib/             # Utility functions
├── utils/           # Helper functions
├── hooks/           # Custom React hooks
├── styles/          # Global styles
└── main.tsx         # Entry point
```

## Development Workflow

1. Create components in `src/components/`
2. Use Tailwind for styling
3. Import shadcn/ui components as needed
4. Test responsive behavior
5. Validate accessibility

## Performance Considerations

- Code splitting for routes
- Image optimization
- Lazy loading for components
- Minimize bundle size
- Optimize CSS delivery

## Browser Support

- Chrome/Edge: Latest 2 versions
- Firefox: Latest 2 versions
- Safari: Latest 2 versions
- Mobile browsers: Latest versions

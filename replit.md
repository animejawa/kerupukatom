# Kerupuk Atom - Landing Page

## Overview

This is a static landing page for "Kerupuk Atom," an Indonesian snack (crackers) brand. The website showcases a single premium product with an interactive carousel showing the product from 6 different angles/perspectives. Built with vanilla HTML, CSS, and JavaScript without any frameworks, making it lightweight and easy to deploy.

## Recent Changes

**November 24, 2025 - Carousel Implementation**
- Replaced multi-product grid with single product showcase
- Implemented interactive carousel with 6 product views (packaging, front view, side angle, top view, detail/close-up, texture)
- Added carousel controls: previous/next buttons and dot indicators
- Auto-play carousel every 5 seconds with pause on hover
- Added product specifications section (texture, flavor, packaging, shelf life)
- Improved accessibility with proper ARIA labels and keyboard support

## User Preferences

Preferred communication style: Simple, everyday language.
Product focus: Single product (Kerupuk Atom Original) displayed with carousel from various angles.

## System Architecture

### Frontend Architecture

**Single-Page Application (SPA) Approach**
- Pure vanilla JavaScript implementation without frameworks (React, Vue, etc.)
- Rationale: Simplicity and minimal dependencies for a static marketing site
- All content lives in one HTML file with anchor-based navigation
- Pros: Fast loading, easy to maintain, no build process required
- Cons: Limited scalability for complex interactive features

**CSS Architecture**
- Custom CSS with CSS variables for theming
- Mobile-first responsive design approach (tablet: 768px, mobile: 480px)
- CSS custom properties (`:root` variables) for consistent color scheme and spacing
- Rationale: Provides flexibility and maintainability without CSS preprocessors
- Gradient-based design system (primary: #667eea, secondary: #764ba2, accent: #f093fb)

**JavaScript Implementation**
- Event-driven DOM manipulation for carousel functionality
- Intersection Observer API for scroll animations
- Accessible navigation with ARIA attributes
- Keyboard support for carousel (Enter key for navigation buttons)
- Auto-play carousel with 5-second intervals
- Rationale: Modern browser APIs provide necessary functionality without libraries
- Pros: No dependencies, better performance, smaller bundle size

**Component Structure**
- Navigation bar: Fixed position with hamburger menu for mobile, smooth hide/show on scroll
- Hero section: Full-screen landing with animated CTA button
- Products section: Single product showcase with:
  - Interactive carousel (6 slides with different product angles)
  - Previous/Next buttons with hover effects
  - Dot indicators for slide navigation
  - Auto-play functionality
  - Product details panel with specifications
  - Feature tags (Renyah, Gurih, Halal, Higienis)
- Gallery section: 6 showcase items (kemasan premium, kualitas terjaga, proses produksi, award winning, tim profesional, dibuat dengan cinta)
- About section: Company information with key features
- Contact section: Contact information cards (alamat, telepon, email, jam operasional)

### Design Patterns

**Progressive Enhancement**
- Base functionality works without JavaScript
- Enhanced features (animations, carousel, mobile menu) added via JavaScript
- Semantic HTML structure ensures accessibility and SEO

**Accessibility Considerations**
- ARIA labels and attributes for screen readers
- Keyboard navigation support for carousel (Enter key)
- Proper focus management for interactive elements
- Hamburger button with ARIA expanded state
- All buttons have descriptive aria-labels

**Animation Strategy**
- CSS-based animations for performance
- Intersection Observer for scroll-triggered animations
- Fade-in delays for staggered content reveal
- Carousel slide transitions with 0.5s ease
- Auto-play carousel every 5 seconds
- Rationale: CSS animations are GPU-accelerated and performant

**Carousel Implementation**
- Manual controls: Previous/Next buttons, clickable dot indicators
- Auto-play: Transitions every 5 seconds
- Pause on hover: Stops auto-play when user hovers over carousel
- Keyboard support: Can navigate with Enter key
- 6 slides showing product from different perspectives with emoji icons and descriptive labels

## External Dependencies

### Third-Party Services

**Google Fonts**
- Font family: Poppins (weights: 300, 400, 600, 700)
- Preconnect optimization for faster font loading
- Rationale: Professional typography without hosting custom fonts

### Browser APIs

**Intersection Observer API**
- Purpose: Trigger animations when elements enter viewport
- Browser compatibility: Modern browsers (IE11 requires polyfill)

**Scroll Events**
- Purpose: Dynamic navbar shadow effect based on scroll position

### No Backend Infrastructure
- Static site with no server-side processing
- No database requirements
- No authentication system
- Deployment: Can be hosted on any static file server (Netlify, Vercel, GitHub Pages, Replit static hosting, etc.)

### Asset Management
- Gradient backgrounds and emoji icons used instead of images
- CSS and JavaScript loaded directly without bundlers
- No content management system integration
- Lightweight with no external JavaScript libraries

## File Structure

```
./
├── index.html      # Main HTML file with semantic structure
├── style.css       # CSS with responsive design (768px and 480px breakpoints)
├── script.js       # JavaScript for carousel, navigation, and animations
└── replit.md       # Project documentation
```

## Deployment

The project is ready to deploy as a static site. It can be hosted on:
- Replit (using the built-in web hosting)
- Netlify
- Vercel
- GitHub Pages
- Any static file server

Currently running on Python HTTP server on port 5000 for development.

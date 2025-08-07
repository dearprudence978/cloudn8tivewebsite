# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page website for Cloudn8tive, a company providing AI observability, Human-in-the-Loop (HITL), and SRE services. The website is built as a pure HTML/CSS/JavaScript application with no build process or external dependencies.

## Architecture

- **Single HTML file**: `index.html` contains the entire website
- **Embedded CSS**: All styles are included in a `<style>` tag within the HTML head
- **Embedded JavaScript**: All functionality is implemented in a `<script>` tag at the end of the HTML body
- **External CDN dependencies**:
  - Tailwind CSS (via CDN)
  - Font Awesome icons (via CDN)
  - Google Fonts (Inter font family)
- **Images**: Located in `/images/` directory, with fallback to placeholder services for external images

## Key Components

### Services System
- Dynamic service cards and modals generated from JavaScript data array (`servicesData`)
- Six main services: AI Observability, HITL, Disaster Recovery, AI Sandboxes, BPO Services, DevOps/SRE
- Modal system for detailed service information

### Interactive Features
- Mobile-responsive navigation with hamburger menu
- Contact form with simulated submission (currently no backend)
- Service modal system with overlay and animations
- Smooth scrolling navigation
- Header scroll effects

### Styling
- Dark theme with brand green (#4ade80) accents
- Tailwind CSS utility classes
- Custom CSS variables for brand colors
- Responsive grid layouts
- Hover animations and transitions

## Development Workflow

### Local Development
- No build process required
- Simply open `index.html` in a web browser
- All assets are either embedded or loaded from CDN

### File Structure
```
/
├── index.html          # Main website file
├── images/            # Image assets
│   ├── White logo - no background.png
│   └── photo-1521737711867-e3b97375f902.avif
└── CLAUDE.md          # This file
```

### Making Changes
- All HTML, CSS, and JavaScript modifications are made directly in `index.html`
- The file is self-contained with embedded styles and scripts
- External image references include `onerror` fallbacks to placeholder services

### Content Management
- Service information is stored in the `servicesData` JavaScript array (lines 374-459)
- Contact information and company details are hardcoded in HTML
- SEO metadata and structured data are included in the HTML head

## Technical Notes

- No package.json, build tools, or dependency management
- No testing framework (consider adding basic HTML validation)
- Contact form currently uses simulated submission - needs backend integration for production
- Images use fallback URLs for reliability
- Responsive design uses Tailwind CSS breakpoints
- All JavaScript is vanilla ES6+ with no external libraries
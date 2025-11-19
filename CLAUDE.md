# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository hosts legal documents (Privacy Policy & Terms of Service) for mobile applications, served as static HTML files. It's a simple static site that provides a centralized location for all app legal documentation.

## Repository Structure

```
/
├── index.html          # Landing page listing all apps
├── temp.html          # Template file for new app legal docs
├── aura/              # Aura Battery Monitor app legal docs
│   ├── privacy.html   # Privacy policy
│   └── terms.html     # Terms of service
└── [app-name]/        # Pattern for additional apps
    ├── privacy.html
    └── terms.html
```

## Architecture

### Multi-App Legal Document Hub
- Each mobile app gets its own subdirectory (e.g., `/aura/`, `/another-app/`)
- Each app directory contains two HTML files: `privacy.html` and `terms.html`
- The root `index.html` serves as a navigation hub linking to all apps' legal documents
- `temp.html` serves as a template for creating new app legal pages

### HTML Design Pattern
All HTML files follow a consistent design system:
- **Styling**: Self-contained CSS using Apple-inspired design (SF Pro fonts, gradient backgrounds)
- **Color Scheme**: Purple gradient theme (`#667eea` to `#764ba2`)
- **Responsive**: Mobile-first design with media queries for tablets/phones
- **Navigation**: Back links to main index for easy navigation
- **Structure**: Semantic HTML with clear section headers

### Legal Document Content Structure

**Privacy Policy** (`privacy.html`):
- Data collection practices (all processing is local/on-device)
- iOS API usage disclosure
- Third-party services (typically none)
- Data storage information
- Apple Intelligence integration (if applicable)
- GDPR/CCPA compliance statements

**Terms of Service** (`terms.html`):
- Service description
- User eligibility requirements
- Permitted and prohibited uses
- Subscription tiers and pricing (Free, Pro, Pro+)
- Auto-renewal terms
- Disclaimers and liability limitations
- Contact information

## Adding a New App

When adding legal documents for a new app:

1. Create a new directory: `mkdir [app-name]`
2. Use `temp.html` as a starting template
3. Create `privacy.html` and `terms.html` in the app directory
4. Update the app-specific content:
   - App name and emoji in the header
   - Last Updated date
   - App-specific features and data usage
   - Contact information
   - Subscription tiers (if applicable)
5. Add an entry to `index.html` linking to the new documents

## Key Conventions

### Date Format
Use format: "Month Day, Year" (e.g., "October 16, 2025")

### Styling Consistency
- Container max-width: 800px
- Border radius: 20px for containers, 12px for cards
- Padding: 50px for desktop, 30px 20px for mobile
- Purple accent color: `#8B5CF6`
- Link color: `#3B82F6`

### Contact Information
Update contact details to match the specific app:
- Email: support@[app-name].com
- Website: https://[app-name].com/support

### Subscription Tiers (if applicable)
Standard tier structure for iOS apps:
- Free tier: Basic features
- Pro: $4.99/year with enhanced features
- Pro+: $9.99/year with advanced features and Family Sharing

## File Maintenance

### No Build Process
This is a static HTML repository. No build, compilation, or deployment commands needed. Files are served as-is.

### Version Control
- Use git for version control
- Commit after adding/updating each app's legal documents
- Tag commits when major policy changes are made

### Testing
Open HTML files directly in a browser to verify:
- Layout and responsive design
- All navigation links work correctly
- Content is properly formatted
- Mobile view renders correctly

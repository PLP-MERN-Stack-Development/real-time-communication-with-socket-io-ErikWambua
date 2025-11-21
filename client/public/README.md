# Public Assets Directory

This directory contains static assets that are served directly by Vite.

## Directory Purpose

Files in this directory:
- Are copied to the build output directory as-is
- Can be referenced using absolute paths in your application
- Are not processed by Vite's build system
- Should be used for assets that don't change

## Recommended Assets

### Favicon
- `favicon.ico` - Browser tab icon
- `favicon-16x16.png` - 16x16 favicon
- `favicon-32x32.png` - 32x32 favicon
- `apple-touch-icon.png` - iOS home screen icon

### App Icons
- `logo.svg` or `logo.png` - Application logo
- `icon-192.png` - PWA icon (192x192)
- `icon-512.png` - PWA icon (512x512)

### Meta Images
- `og-image.png` - Open Graph image for social media (1200x630)
- `twitter-card.png` - Twitter card image

### Other
- `robots.txt` - Search engine crawling rules
- `manifest.json` - PWA manifest file
- `sitemap.xml` - Site map for SEO

## Usage

Reference files from this directory using absolute paths:

```html
<!-- In index.html -->
<link rel="icon" href="/favicon.ico" />
<link rel="apple-touch-icon" href="/apple-touch-icon.png" />

<!-- In components -->
<img src="/logo.png" alt="App Logo" />
```

## Note

For images imported in components, consider using:
- Import statements: `import logo from '../assets/logo.png'`
- This allows Vite to optimize and bundle the images

Only use the public directory for:
- Files that must maintain exact filenames
- Assets referenced in `index.html`
- Files needed by external services (robots.txt, etc.)

# Progressive Web App (PWA) & SPA Production Blueprint

## Core Architecture Standards
* **Mobile-First Responsive UI:** Zero horizontal scroll across 320px to 4K viewports.
* **Offline & Caching Strategy:** Service Worker with Network-First strategy for dynamic API calls and Cache-First for static assets.
* **Installability:** Valid `manifest.json` with maskable icons, standalone display mode, and custom theme colors.
* **Clean URL Routing:** Extensionless clean URLs via `.htaccess` / server rewrite rules.

## Sample `manifest.json`

```json
{
  "name": "Enterprise PWA Starter",
  "short_name": "PWAApp",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#0f172a",
  "icons": [
    {
      "src": "/icons/icon-192.webp",
      "sizes": "192x192",
      "type": "image/webp"
    },
    {
      "src": "/icons/icon-512.webp",
      "sizes": "512x512",
      "type": "image/webp"
    }
  ]
}

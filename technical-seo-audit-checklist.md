# Technical SEO & Structured Data Audit Checklist

## 1. Crawlability & Indexing
* Clean `robots.txt` without blocking critical CSS/JS assets.
* Dynamic XML Sitemap submitted to Google Search Console with only `200 OK` canonical URLs.
* Proper `301` permanent redirects (HTTP to HTTPS, non-www to www) with zero redirect chains.
* Self-referencing `<link rel="canonical">` tags on every indexable page.

## 2. On-Page & Architecture
* Single `<h1>` per page matching primary search intent, followed by logical `<h2>`–`<h3>` hierarchy.
* Unique `<title>` (50–60 chars) and `<meta name="description">` (140–155 chars).
* Next-gen compressed images (`WebP`) with explicit `width` and `height` attributes to prevent layout shift.

## 3. Sample JSON-LD Structured Data (Professional Service)

```json
{
  "@context": "[https://schema.org](https://schema.org)",
  "@type": "ProfessionalService",
  "name": "Prayag Kaushik - Full Stack, QA & Accessibility Consulting",
  "url": "[https://www.prayaggkaushikk.com/](https://www.prayaggkaushikk.com/)",
  "areaServed": "Worldwide",
  "knowsAbout": [
    "Full Stack Web Development",
    "Progressive Web Apps (PWA)",
    "QA Automation",
    "WCAG 2.2 Accessibility Auditing",
    "Technical SEO"
  ]
}

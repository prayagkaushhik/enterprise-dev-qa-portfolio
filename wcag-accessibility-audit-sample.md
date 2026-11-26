# WCAG 2.2 (Level AA) & Section 508 Accessibility Audit Framework

**Auditor:** Prayag Kaushik (DHS Section 508 Trusted Tester Certified)

## 1. Key Audit Checkpoints
* **Perceivable:** Meaningful `alt` attributes for informative images, empty `alt=""` for decorative graphics, minimum 4.5:1 color contrast ratio for normal text.
* **Operable:** Full keyboard navigation (`Tab`, `Shift+Tab`, `Enter`, `Esc`), visible focus indicators, zero keyboard traps, skip-to-main-content links.
* **Understandable:** Explicit `<label for="...">` associations on all form inputs, clear inline error announcements (`aria-live="polite"`), proper `<html lang="en">` declaration.
* **Robust:** Semantic HTML5 landmarks (`<header>`, `<nav>`, `<main>`, `<footer>`), valid ARIA roles, tested with **NVDA Screen Reader** and **Axe DevTools**.

---

## 2. Accessible Form Pattern (WCAG 2.2 Compliant)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Accessible Contact Form Sample</title>
</head>
<body>
  <a href="#main-content" class="skip-link">Skip to main content</a>
  
  <main id="main-content">
    <h1>Request a Project Consultation</h1>
    <form action="/submit" method="POST" novalidate>
      <div>
        <label for="client-name">Full Name <span aria-hidden="true">*</span></label>
        <input id="client-name" name="name" type="text" required aria-required="true" />
      </div>

      <div>
        <label for="client-email">Business Email <span aria-hidden="true">*</span></label>
        <input id="client-email" name="email" type="email" required aria-required="true" aria-describedby="email-hint" />
        <small id="email-hint">We will send your audit report to this address.</small>
      </div>

      <button type="submit">Submit Request</button>
    </form>
  </main>
</body>
</html>

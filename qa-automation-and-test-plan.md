# Enterprise QA Strategy & Automation Sample

**Author:** Prayag Kaushik (ISTQB CTFL | 15+ Years QA & Dev Experience)

## 1. End-to-End QA Release Checklist
* **Functional & Regression:** Core user flows, boundary value analysis, negative testing, API response validation.
* **Cross-Browser & Device Matrix:** Chrome, Edge, Safari, Firefox (Desktop + Android/iOS mobile viewports).
* **Performance & Core Web Vitals:** LCP < 2.5s, CLS < 0.1, INP < 200ms verification before production sign-off.
* **Security Basics:** HTTPS enforcement, input sanitization, XSS/CSRF sanity checks, session timeout validation.

---

## 2. Sample Automated Smoke Test (Python + Playwright)

```python
from playwright.sync_api import sync_playwright

def test_critical_user_journey():
    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True)
        page = browser.new_page()
        
        # 1. Load Application & Verify Title
        page.goto("[https://example.com](https://example.com)", timeout=15000)
        assert "Example" in page.title(), "Page title mismatch"
        
        # 2. Verify Primary CTA Accessibility & Visibility
        cta_button = page.get_by_role("link", name="More information")
        assert cta_button.is_visible(), "Primary CTA is not visible"
        
        # 3. Validate Navigation & HTTP Status
        response = page.goto("[https://example.com](https://example.com)")
        assert response.status == 200, f"Unexpected status code: {response.status}"
        
        print("Smoke test passed successfully.")
        browser.close()

if __name__ == "__main__":
    test_critical_user_journey()

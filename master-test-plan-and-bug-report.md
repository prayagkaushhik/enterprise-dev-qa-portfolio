# Master QA Test Plan & Defect Triage Sample

**Prepared By:** Prayag Kaushik (ISTQB CTFL | 15+ Years QA & Dev Experience)

## 1. Test Scope & Objectives
* Validate end-to-end business workflows, UI responsiveness, API/form behavior, cross-browser compatibility, accessibility, and SEO readiness prior to production release.
* Identify high-impact defects early to reduce rework and release delays.

## 2. Entry & Exit Criteria
* **Entry Criteria:** Build deployed to staging/QA environment, core smoke paths accessible, test data prepared, and release scope defined.
* **Exit Criteria:** 100% of critical/high test cases executed, zero open Blocker/Critical defects, agreed workarounds for minor items, and QA sign-off completed.

## 3. Risk & Severity Matrix
* **Blocker / Critical:** Application crash, broken checkout/payment/auth flow, data loss, or severe security/accessibility barrier blocking core tasks.
* **Major:** Important feature fails with a partial workaround, layout breakage on key viewports, or incorrect validation logic.
* **Minor:** Cosmetic alignment issues, non-blocking copy typos, or minor UI polish items.

## 4. Sample Defect Report Format

| Field | Details |
| :--- | :--- |
| **Bug ID** | `BUG-QA-104` |
| **Title** | Checkout submit button remains disabled after valid input on mobile viewport |
| **Severity / Priority** | Critical / P1 |
| **Environment** | Android Chrome / Desktop Edge, Staging Build v2.4.1 |
| **Steps to Reproduce** | 1. Open product page and add item to cart.<br>2. Navigate to checkout and enter valid name, email, and payment details.<br>3. Tap **Pay Now**. |
| **Expected Result** | Form validates cleanly and proceeds to payment gateway/confirmation. |
| **Actual Result** | Button does not trigger submission and no validation message is shown. |
| **Impact & Recommendation** | Blocks order completion; verify form event listener, validation state, and keyboard/touch focus handling. |

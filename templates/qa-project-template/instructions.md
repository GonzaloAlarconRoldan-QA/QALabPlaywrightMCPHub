# AI QA Automation Instructions

## General Rules

* Always use Playwright browser automation when validating UI behavior.
* Prefer stable selectors such as roles, labels and visible text.
* Avoid brittle CSS selectors whenever possible.
* Avoid hardcoded waits unless absolutely necessary.
* Always run the browser in maximized mode

---

## Exploratory Testing Rules

* Validate critical workflows first.
* Inspect navigation consistency.
* Validate loading states.
* Validate empty states.
* Validate error handling.
* Monitor browser console errors.
* Monitor failed network requests.

---

## Evidence Collection

Always capture:

* screenshots on failures
* screenshots on suspicious UI states
* console errors
* network failures

Store evidence inside:

* screenshots/
* evidence/
* reports/

---

## Findings Documentation

All findings must:

* be written in markdown
* include reproduction steps
* include expected vs actual behavior
* include severity assessment
* include screenshots if applicable

Store findings in:
findings/

Use timestamped filenames.

---

## Regression Identification

When a bug or validation is important:

* recommend regression automation candidates
* suggest Playwright test conversion opportunities

Store recommendations in:
notes/regression-candidates.md

---

## Automation Standards

* Use TypeScript Playwright tests
* Use reusable helpers
* Keep tests isolated
* Keep tests deterministic
* Use retries for flaky environments
* Capture traces on failure

---

## Safety Rules

* Do not execute destructive actions unless explicitly requested.
* Avoid modifying production data.
* Avoid deleting entities unless instructed.
* Prefer read-only exploratory validation when possible.
* Avoid interact with new users registration or anything related to users CRUD

---

## Reporting Style

Reports must be:

* concise
* structured
* actionable
* professional

Always summarize:

* validated workflows
* failed validations
* risks
* recommendations

Also:
* Create playwright HTML report when a test is completed, it should be created with all the information collected (screenshots, test status, performance, load, etc.)

# Purpose
Generate a **production‑ready** Angular 19 standalone component for the SWFT shared library.

# SWFT defaults
- `standalone: true` + `ChangeDetectionStrategy.OnPush`
- Strict typing (no `any`), small private helpers
- One `@Input()` + one `@Output()` (typed)
- `isLoading` flag; disable actions while loading
- a11y: semantic HTML, `ariaLabel` where relevant, focus management
- Errors via snack‑bar/alert (no console logs)
- SCSS only (no inline styles)
- Subscriptions via **SubSink**
- Export from `public-api.ts` if shared

# Always generate these files
- `<kebab-name>.component.ts`
- `<kebab-name>.component.html`
- `<kebab-name>.component.scss`
- `<kebab-name>.component.spec.ts` (Jest: happy + error + event)

# Location
`projects/swft/swft-ngx-eform-trigger-shared/components/<feature>/<kebab-name>/`

# Example
Name: `SwftEformSummaryComponent`  
Feature: `shared`  
Path: `projects/swft/swft-ngx-eform-trigger-shared/components/shared/swft-eform-summary/`

---
## What to type in Copilot Chat
Create a production‑ready shared component **SwftEformSummaryComponent** under `components/shared/swft-eform-summary/`.  
Follow SWFT rules (standalone, OnPush, strict typing, `isLoading`, a11y, SubSink) and include TS/HTML/SCSS + a Jest spec with happy, error, and event tests.

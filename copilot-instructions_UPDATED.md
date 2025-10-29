# Copilot Instructions – SWFT Angular Library (UPDATED)

This repo is part of the SWFT shared Angular setup. The goal is to make Copilot follow the same structure, naming, and coding style we use across all SWFT libraries.

---
## Project Overview
Angular 19, standalone components, Jest for unit testing, strict TypeScript. All code should align with SWFT shared patterns.

**Library:** `swft-ngx-eform-trigger-shared`  
**Primary folders:** `components/`, `constants/`, `models/`, `services/`, `utils/`

Each new feature lives in its own folder under the right category (e.g., `components/shared/eform-summary`).

---
## Key Guidelines
- Standalone components with `ChangeDetectionStrategy.OnPush`
- Strict typing (no `any`)
- Use Angular Material + Kendo already in the project
- `isLoading` for async actions; snack-bar for errors
- No hardcoded UI strings in logic — use constants
- Use **SubSink** for subscriptions cleanup
- Accessibility: labels, roles, focus mgmt
- SCSS only — no inline styles
- Keep files separate (TS/HTML/SCSS/spec)
- Avoid console logs in final code

---
## Folder & File Structure (example)
```
projects/swft/swft-ngx-eform-trigger-shared/
  components/
    shared/
      swft-eform-summary/
        swft-eform-summary.component.ts
        swft-eform-summary.component.html
        swft-eform-summary.component.scss
        swft-eform-summary.component.spec.ts
  constants/
  models/
  services/
  utils/
  public-api.ts
```
---
## Generation Defaults (production-ready)
Whenever Copilot creates or updates code, assume:
- Angular 19 **standalone** + `OnPush`
- Strict typing; small private helpers
- `isLoading` + disabled UI during async
- Errors via snack-bar/alert (no console logs)
- **Tests included**: Jest, happy + error + event paths (aim 80%+)
- Accessibility: semantic markup, `ariaLabel`, focus mgmt
- SCSS only (no inline styles)
- Subscriptions via **SubSink**
- Follow folder structure and export from `public-api.ts` when shared

### Generation Behavior
For **components** and **dialogs**, Copilot should automatically:
- Create **all four files** (TS, HTML, SCSS, spec)
- Use **standalone** + **OnPush**
- Add one example `@Input()` + one `@Output()`
- Include an `isLoading` flag and snack-bar error handling
- Add accessibility roles/labels and keyboard focus
- Place files under the path shown above

For **services**, Copilot should automatically:
- Use `@Injectable({ providedIn: 'root' })` and `HttpClient`
- Use typed DTOs (no `any`); `catchError` and minimal `retry`
- Generate a Jest spec using `HttpTestingController`

---
## What to type in Copilot Chat (copy-paste examples)

### A) Full feature scaffold (component + service + models + tests)
Create a new shared feature **SwftEformSummary**.  
Generate a standalone component with OnPush under `components/shared/swft-eform-summary/` (TS/HTML/SCSS/spec with happy+error+event tests).  
Create **SwftEformSummaryService** under `services/shared/` with typed DTOs in `models/` and a Jest spec using `HttpTestingController`.  
Add an `isLoading` flag, snack‑bar error handling, and accessibility labels. Export shared artifacts from `public-api.ts`.

### B) Component (includes TS/HTML/SCSS/Jest)
Create a production‑ready shared component **SwftEformSummaryComponent** under `components/shared/swft-eform-summary/`.  
Follow our SWFT rules (standalone, OnPush, strict typing, `isLoading`, a11y, SubSink) and include a Jest spec with happy, error, and event tests.

### C) Dialog (includes TS/HTML/SCSS/Jest)
Create a Material dialog **SwftEformPreviewDialog** under `components/shared/swft-eform-preview/`.  
Use `MAT_DIALOG_DATA` for input, `MatDialogRef` to return results, add `ariaLabel` + `autoFocus`, loading state, and snack‑bar error handling. Include a Jest spec for open/close and data in/out.

### D) Service (includes test)
Create **SwftEformSummaryService** in `services/shared/` with `HttpClient`, typed DTOs from `models/`, `catchError` and minimal `retry`. Generate a Jest test using `HttpTestingController` (success + error).

### E) Tests only for an existing component
Write production‑grade Jest tests for **SwftEformSummaryComponent** at `components/shared/swft-eform-summary/`. Cover happy path, error path, and output event; mock `MatDialog`/`MatSnackBar` as needed.

---
## Prompts Reference
Custom prompts live in `.github/prompts/` (component, dialog, service, feature scaffold, tests, code review).

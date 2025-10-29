# Purpose
Generate a **production‑ready** Angular 19 standalone component that follows SWFT shared‑library patterns.

# Requirements
- Location: `projects/swft/swft-ngx-eform-trigger-shared/components/<feature>/<component-name>/`
- `ChangeDetectionStrategy.OnPush`; strict typing; no `any`
- Inputs/Outputs: at least one of each (typed)
- State: `isLoading` flag; disabled UI during async
- Accessibility: semantic HTML, `ariaLabel` where relevant
- UX: snack‑bar/alert for errors (no console logs)
- Styling: SCSS file; no inline styles
- Tests: **Jest** spec with happy path, error path, and event tests (80%+ intent)
- Export from `public-api.ts` if this is a shared piece

# Output files
- `<component>.component.ts` (standalone + OnPush)
- `<component>.component.html`
- `<component>.component.scss`
- `<component>.component.spec.ts`

# Example
Name: `SwftEformSummaryComponent`
Feature: `shared`

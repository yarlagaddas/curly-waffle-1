# Purpose
Scaffold a **production‑ready feature slice** (component + service + models + tests) for the SWFT shared library.

# What to generate
1) Component (standalone + OnPush) with HTML/SCSS/spec under:
   `projects/swft/swft-ngx-eform-trigger-shared/components/<feature>/<component-name>/`
2) Service with spec under:
   `projects/swft/swft-ngx-eform-trigger-shared/services/<feature>/<service-name>.service.ts`
3) Models (typed interfaces) under:
   `projects/swft/swft-ngx-eform-trigger-shared/models/`
4) Add/ensure export in `public-api.ts` for shared artifacts

# Rules
- Strict typing; no `any`
- `isLoading` + error display via snack‑bar
- A11y: semantic markup + labels
- Tests for both component and service (happy + error paths)
- Use constants for UI strings; keep logic clean

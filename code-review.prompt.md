# Purpose
Perform a **production‑readiness** review for an Angular PR in the SWFT shared library.

# Checklist
- Architecture: standalone component; `OnPush` used appropriately
- Structure: files in correct folders; exported via `public-api.ts` if shared
- Typing: no `any`; clear interfaces in `models/`
- State: `isLoading`/disable during async; errors via snack‑bar
- A11y: `ariaLabel`/roles; keyboard focus in dialogs
- RxJS: subscriptions managed with SubSink; cleaned up
- Tests: Jest present; happy + error paths; meaningful assertions
- Style: SCSS only; theming consistent; no inline styles
- Strings: constants/i18n‑ready; nothing hardcoded in logic

# Output format
Group findings by ✅ Passed / ⚠️ Needs Attention / ❗ Blocker with actionable suggestions.

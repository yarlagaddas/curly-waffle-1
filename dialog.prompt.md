# Purpose
Create a **production‑ready** Angular Material dialog component consistent with SWFT standards.

# Requirements
- Uses `MatDialog` + `MAT_DIALOG_DATA` + `MatDialogRef`
- Accessibility: `ariaLabel`, `role="dialog"`, focus trap/`autoFocus`
- Title/labels via constants (no hardcoded strings in logic)
- Loading state + error handling (snack‑bar)
- SCSS only; no inline styles
- Tests: Jest spec covering open/close, data in/out, and error path

# Output files
- `<name>.dialog.ts` (standalone + OnPush)
- `<name>.dialog.html`
- `<name>.dialog.scss`
- `<name>.dialog.spec.ts`

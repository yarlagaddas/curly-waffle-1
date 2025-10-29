# Purpose
Create a **production‑ready** Angular service for the SWFT shared library.

# Requirements
- `@Injectable({ providedIn: 'root' })`
- `HttpClient` with typed DTOs from `models/`
- Error handling with `catchError()`; consider `retry()` where sensible
- Logging via shared UI (snack‑bar) or error service, not console logs
- Tests: Jest with `HttpTestingController` (success + error)

# Output
- `services/<feature>/<name>.service.ts`
- `services/<feature>/<name>.service.spec.ts`

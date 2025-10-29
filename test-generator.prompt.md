# Purpose
Generate **production‑grade Jest tests** for a component or service.

# Requirements
- Use `TestBed` (`HttpTestingController` for services)
- Cover: happy path, error path, and key events/outputs
- Mock: MatDialog/MatSnackBar or HttpClient as needed
- Target: meaningful assertions; avoid testing framework internals

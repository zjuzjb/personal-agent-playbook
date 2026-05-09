# Bugfix Flow

Default flow for bugs and regressions.

1. Reproduce or inspect the smallest useful failing path.
2. Identify root cause before changing code.
3. Define scope and non-goals.
4. Patch the narrowest behavior that fixes the root cause.
5. Add or update regression coverage when practical.
6. Re-run the failing path and relevant checks.
7. Report any unrelated failures separately.


---
description: Run Slopwatch quality gate for .NET projects
---
Run Slopwatch as an explicit, invocable command.

1. Verify tool is available:
   - Prefer local manifest: `dotnet tool restore`
   - If unavailable, install globally: `dotnet tool install --global Slopwatch.Cmd`

2. Run analysis in strict mode:
   - `slopwatch analyze -d . --fail-on warning`

3. If findings exist:
   - Summarize by rule (SW001-SW006)
   - Include file and line for each finding
   - Recommend concrete remediation (do not suppress)

4. If no findings:
   - Report pass and remind to keep baseline intentional

Never auto-update baseline unless the user explicitly requests it.

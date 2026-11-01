---
name: code-quality-check
description: Review code changes against applicable coding conventions and report actionable quality issues without modifying files.
disable-model-invocation: true
argument-hint: "[files, directory, or changes]"
---

# Code Quality Check

Review the specified code scope: $ARGUMENTS

If no scope is provided, review the current uncommitted changes, including relevant untracked files. If no changes exist, ask for a review scope.

## Review Process

1. Read the applicable coding rules and project conventions.
2. Inspect the relevant code and its surrounding context.
3. Evaluate the code against the checklist below.
4. Report actionable findings supported by the inspected code.

## Code Quality Checklist

- [ ] Code is readable, well-named, and follows project conventions.
- [ ] Functions have clear responsibilities and consistent levels of abstraction.
- [ ] Files and modules are cohesive and maintainable.
- [ ] Control flow is clear and avoids unnecessary complexity.
- [ ] Errors are handled appropriately.
- [ ] Meaningful thresholds, limits, and configuration values are named.
- [ ] State changes are intentional and controlled.
- [ ] Comments are limited to non-obvious behavior and constraints.

## Review Output

- List findings by severity, with file and line references.
- Explain each issue and suggest a focused improvement.
- Summarize the checklist results.
- Distinguish verified findings from uncertainties.
- If no actionable issues are found, state that explicitly.

## Constraints

- Do not modify files.
- Do not introduce new coding conventions.
- Do not suggest refactoring without a clear maintainability benefit.
- Do not claim that tests or other checks passed unless they were executed.
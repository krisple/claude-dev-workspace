# Coding Style

## Immutability

Prefer immutable data by default; use mutation when it is simpler or necessary.

Rationale: Immutability reduces unintended side effects and improves concurrency safety, but mutation can be simpler or more efficient in certain cases.

## Core Principles

### KISS (Keep It Simple)

- Prefer the simplest solution that meets the requirements
- Avoid premature optimization
- Optimize for clarity over cleverness

### DRY (Don't Repeat Yourself)

- Extract repeated logic into shared functions or utilities
- Avoid copy-paste implementation drift
- Introduce abstractions when repetition is real, not speculative

### YAGNI (You Aren't Gonna Need It)

- Do not build features or abstractions before they are needed
- Avoid speculative generality
- Start simple, then refactor when the pressure is real

## File Organization

- Keep files and modules focused on clear, well-defined responsibilities.
- Maintain high cohesion and low coupling.
- Prefer organizing by feature/domain while following language and framework conventions.

## Error Handling

- Handle errors at the appropriate level; propagate them when necessary.
- Provide clear, user-friendly error messages in UI-facing code.
- Log sufficient context for debugging without exposing sensitive information.
- Never silently swallow unexpected errors.

## Input Validation

- Validate untrusted data at system boundaries, including user input, API responses, and file content.
- Use schema-based validation when appropriate.
- Reject invalid input early with clear error messages.

## Naming Conventions

- Use descriptive, meaningful names that clearly communicate purpose.
- Name boolean variables to express the condition they represent.
- Follow established language and framework naming conventions for identifiers, types, and constants.

## Code Smells to Avoid

### Deep Nesting

Prefer early returns over nested conditionals once the logic starts stacking.

### Magic Numbers

Use named constants for meaningful thresholds, delays, and limits.

### Function Structure

- Keep each function focused on a single responsibility and a consistent level of abstraction.
- Express high-level workflows through a sequence of intention-revealing function calls.
- Extract implementation details into well-named functions when it improves readability.

## Comments and Documentation

- Prefer self-documenting code through clear naming and well-structured functions.
- Add comments only to clarify non-obvious behavior or constraints.
- Avoid comments that restate the code or document implementation decisions and development history.
- Document significant architectural decisions separately (e.g., ADRs).

## Code Quality Checklist

Before marking work complete:

- [ ] Code is readable, well-named, and follows project conventions.
- [ ] Functions have clear responsibilities and consistent levels of abstraction.
- [ ] Files and modules are cohesive and maintainable.
- [ ] Control flow is clear and avoids unnecessary complexity.
- [ ] Errors are handled appropriately.
- [ ] Meaningful thresholds, limits, and configuration values are named.
- [ ] State changes are intentional and controlled.
- [ ] Comments are limited to non-obvious behavior and constraints.
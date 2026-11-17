# Clean code and clean architecture

Use these rules when building or refactoring software. Keep the existing project structure and conventions, and do not add unnecessary layers or architectural ceremony before the need is clear.

## Keep responsibilities clear

- Organize code by business capability and responsibility rather than by implementation detail.
- Keep each module, class, and function focused on one thing and one reason to change.
- Prefer small, explicit units over large, multi-purpose abstractions.
- Name things for intent and behavior, not for the underlying technology or a short abbreviation.
- Reduce coupling by keeping distant concerns separate and by making dependencies explicit.

## Design around the domain

- Put core domain logic and business rules at the center of the design.
- Keep infrastructure concerns such as APIs, database access, UI rendering, and framework code on the edges.
- Depend on abstractions, not concrete implementations, when crossing architectural boundaries.
- Make the flow of dependencies point inward: the domain should not depend on the UI or persistence layer.
- Keep orchestration thin; controllers, route handlers, and use-case entry points should coordinate rather than contain business logic.

## Keep code readable and maintainable

- Write functions that are short, direct, and easy to follow; avoid deep nesting and fantasy abstractions.
- Prefer clear control flow and explicit conditions over clever tricks.
- Encapsulate behavior behind meaningful interfaces or small cohesive objects.
- Avoid hidden side effects and keep state transitions understandable.
- Remove dead code, commented-out blocks, and stale workarounds unless there is a clear reason to keep them.

## Manage complexity intentionally

- Prefer composition over inheritance when a behavior can be explained more simply.
- Split large responsibilities into smaller units with strong boundaries and clear contracts.
- Minimize state sharing; pass required data explicitly and keep scope narrow.
- When a change introduces complexity, refactor the surrounding code so the design stays coherent and understandable.
- Avoid creating abstractions before the repeated need is proven.

## Errors, validation, and reliability

- Validate inputs at the boundaries and fail early with clear, actionable errors.
- Handle exceptions and edge cases explicitly instead of swallowing them silently.
- Keep business rules in one place and avoid duplicating logic across components.
- Prefer deterministic behavior and straightforward data flow when possible.
- Make code testable by isolating side effects and external dependencies.

## Testing and verification

- Add or update focused tests around behavior, edge cases, and regression risks.
- Prefer testing the public behavior of a component rather than its internal implementation details.
- Keep tests readable, meaningful, and close to the business intent they validate.
- Run the smallest relevant checks that confirm the code still behaves correctly.

## Completion checklist

- [ ] Responsibilities are clearly separated and each unit has a single purpose.
- [ ] Domain logic is protected from infrastructure and UI concerns.
- [ ] Dependencies flow inward and boundaries are explicit.
- [ ] Functions and modules are small, understandable, and free from unnecessary complexity.
- [ ] Errors and edge cases are handled clearly and predictably.
- [ ] Relevant tests cover the changed behavior and guard against regressions.

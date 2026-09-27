# AI Coding Agent Instructions

## 1. Purpose

This file defines how the AI coding agent must work with the specifications in this repository.

The agent must implement the Customer Management Service according to the specifications and must not replace explicit requirements with its own assumptions.

---

## 2. Read the Specification First

Before implementation:

1. Read and understand every file under `/specs`.
2. Treat `specs/05-openapi.yaml` as the authoritative REST API contract.
3. Treat `specs/03-acceptance-criteria.md` as the required verification criteria.
4. Follow the technical boundaries defined in `specs/04-technical-constraints.md`.
5. Ensure the implementation remains consistent with `specs/01-requirements.md` and `specs/02-system-specification.md`.

Do not begin implementation until the specification has been reviewed.

---

## 3. Implementation Workflow

Before modifying the application:

1. Inspect the repository and all specification files.
2. Create an implementation plan.
3. Map the planned implementation to the requirements and acceptance criteria.
4. Implement the smallest coherent solution that satisfies the specification.
5. Generate automated tests covering the acceptance criteria.
6. Run the complete test suite.
7. Fix implementation failures.
8. Re-run the tests until the implementation satisfies the specification.

---

## 4. API Contract

The REST API must follow `specs/05-openapi.yaml`.

Do not independently change:

- API paths
- HTTP methods
- Request models
- Response models
- Field names
- HTTP status codes
- Defined error responses

If the implementation differs from the OpenAPI contract, change the implementation.

---

## 5. Technical Constraints

Follow all constraints defined in `specs/04-technical-constraints.md`.

In particular:

- Use the approved technology stack.
- Follow the defined layered architecture.
- Do not place business logic in controllers.
- Controllers must not access repositories directly.
- Do not expose JPA entities as external API models.
- Use DTOs for API requests and responses.
- Use Jakarta Validation for input validation.
- Generate unit and integration tests using JUnit 5.
- Keep the implementation modular and maintainable.

---

## 6. Acceptance Criteria

All acceptance criteria in `specs/03-acceptance-criteria.md` are mandatory.

Automated tests should provide evidence that the implementation satisfies these criteria.

A successful build alone does not mean the specification has been satisfied.

---

## 7. Specification Protection

Do not modify specification files merely to make the implementation or tests pass.

The files under `/specs` represent human-defined intent and constraints.

If the implementation conflicts with the specification:

**Change the implementation — not the specification.**

---

## 8. Conflict Handling

If specification documents conflict with each other:

1. Stop implementation of the conflicting behavior.
2. Clearly identify the conflicting specification statements.
3. Report the conflict.
4. Do not invent or assume a resolution.

Implementation may continue only after the conflict has been resolved in the specification.

---

## 9. Scope Control

Do not introduce functionality that is not required by the specification.

Avoid unnecessary frameworks, abstractions, integrations, or features.

Implementation decisions not explicitly constrained by the specification may be made by the coding agent, provided they remain consistent with the requirements and technical constraints.

---

## 10. Completion Criteria

Implementation is complete only when:

- The application builds successfully.
- The REST API matches the OpenAPI contract.
- All acceptance criteria are satisfied.
- Automated tests pass.
- Technical constraints are respected.
- No specification files were changed to accommodate implementation behavior.

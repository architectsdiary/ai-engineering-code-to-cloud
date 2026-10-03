# Agent Instructions

## Read before coding
Read and understand, in this order:
1. `business/01-business-requirements.md`
2. `architecture/01-system-context.md`
3. `architecture/02-domain-model.md`
4. `architecture/03-technical-principles.md`
5. all files under `specs/user-management/`

Business and architecture documents provide intent and boundaries. The current increment specification defines required behavior. Acceptance criteria are mandatory. `05-openapi.yaml` is authoritative for the REST contract.

## Engineering rules
- Implement only the current approved increment.
- Do not implement future capabilities merely because they appear in the product vision.
- Keep domain/capability boundaries explicit.
- Do not expose JPA entities directly through REST.
- Use separate API DTOs and persistence models with explicit mapping.
- Keep controllers thin; business behavior belongs in the service/application layer.
- Use consistent structured error responses.
- IDs and audit timestamps are server controlled.
- Add automated tests for required behavior.
- Run the complete test suite before declaring the increment complete.
- Never change specifications merely to make implementation or tests pass.
- If specifications conflict or are ambiguous, report the issue rather than inventing business behavior.

## Working lifecycle
Read → Understand → Plan → Implement → Build → Test → Fix → Verify.

For later increments, first inspect the existing application and perform impact analysis before implementation. Protect existing behavior with regression tests.

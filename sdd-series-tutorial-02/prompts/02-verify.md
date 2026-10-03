# Verification Prompt

Verify the implementation against:
- `AGENTS.md`
- business requirements
- system context
- domain model
- technical principles
- all User Management specification files
- `05-openapi.yaml`

Do not modify the specification during verification.

Check:
- required technology stack and application structure
- every functional requirement and business rule
- system behavior
- every acceptance criterion
- REST paths, methods, request/response schemas, and status codes
- DTO/entity separation
- validation and structured errors
- scope boundaries
- automated test coverage

Run the complete build and test suite.

For each finding, report one of:
- PASS
- FAIL
- PARTIAL
- NOT TESTED

For FAIL or PARTIAL, explain the mismatch and the required correction.

Finish with the build/test result and any unresolved specification compliance issues.

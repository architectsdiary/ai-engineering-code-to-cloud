# Implementation Prompt

Read `AGENTS.md`, then read the business, architecture, and complete User Management specification before changing code.

Create the initial `mini-ecom-backend` application and implement the User Management increment.

Before coding:
1. Summarize the required behavior and constraints.
2. Propose the package/module structure.
3. Report any conflicts or ambiguities. Do not invent behavior.

Implementation must include:
- Spring Boot application foundation
- User persistence
- roles and lifecycle status
- REST DTOs and explicit mapping
- repository and service/application logic
- REST controller
- validation
- structured error handling
- automated tests
- springdoc/OpenAPI support

Implement only the current increment. Do not add future capabilities.

After implementation:
1. Compile the project.
2. Run the complete automated test suite.
3. Fix implementation defects.
4. Verify the REST contract against `05-openapi.yaml`.
5. Report what was implemented and the final build/test result.

Never modify the specification merely to make implementation or tests pass.

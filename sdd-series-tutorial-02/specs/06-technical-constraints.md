# Technical Constraints
Modify the existing `mini-ecom-backend`; do not generate a second application.

Java 21, Spring Boot 3.x, Maven, Spring Web, Spring Data JPA, Jakarta Validation, H2, JUnit 5, OpenAPI 3.x/springdoc.

Package root: `com.architectsdiary.miniecom`. Prefer capability packages such as `customer`, `user`, `common`.

OpenAPI is authoritative for the new User REST interface. Existing Customer contracts are regression constraints unless explicitly changed.

Continue H2. Do not add PostgreSQL/Flyway yet. Add User tests and run Customer regression tests. Build and full test suite must pass.

If specifications conflict with each other or existing behavior, report the conflict rather than silently changing specifications.

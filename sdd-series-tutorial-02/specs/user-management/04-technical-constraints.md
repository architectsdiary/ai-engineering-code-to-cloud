# User Management — Technical Constraints

## Stack
- Java 21
- Spring Boot 3.x
- Maven
- Spring Web
- Spring Data JPA
- Jakarta Validation
- H2
- JUnit 5
- OpenAPI 3.x with springdoc

## Application
- Project name: `mini-ecom-backend`
- Preferred base package: `com.architectsdiary.miniecom`
- Use capability-oriented organization.
- Separate REST DTOs from JPA entities.
- Use explicit mapping.
- Keep controllers thin.
- Use UUID identifiers.
- Use structured validation, not-found, and conflict errors.

## Persistence
Use Spring Data JPA and H2 for this increment.

Do not introduce PostgreSQL, Flyway, Redis, Kafka, or other infrastructure in Tutorial 02.

## Tests
Automated tests must cover:
- CRUD behavior
- status changes
- role replacement
- multiple roles
- case-insensitive username/email conflicts
- validation failures
- missing User behavior

The final implementation must compile and all tests must pass.

# Technical Principles

- Build a modular Spring Boot application.
- Organize code around business capabilities; avoid premature microservices.
- Keep REST DTOs separate from persistence entities.
- Use explicit mapping between API and persistence models.
- Keep controllers thin.
- Keep business rules in the application/service layer.
- Define REST contracts using OpenAPI.
- Use `/api/v1` as the API base path.
- Return consistent structured errors.
- Use Spring Data JPA for persistence.
- Use H2 for Tutorial 02.
- Introduce production databases and migration tooling in later increments.
- Validate API input with Jakarta Validation.
- Use automated tests for acceptance behavior where practical.
- Later increments must include regression testing for existing behavior.
- Do not implement speculative features.
- API contract changes require an explicit specification change and impact analysis.

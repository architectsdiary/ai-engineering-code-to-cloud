# SDD Series --- Tutorial 01

## Customer Management Service

This folder is the Tutorial 1 version of the original
`sdd-customer-service` project used in the Spec-Driven Development
walkthrough.

We begin with **specifications, agent instructions, and prompts --- not
application code**.

## Project Structure

``` text
sdd-series-tutorial-01/
├── README.md
├── AGENTS.md
├── specs/
│   ├── 01-requirements.md
│   ├── 02-system-specification.md
│   ├── 03-acceptance-criteria.md
│   ├── 04-technical-constraints.md
│   └── 05-openapi.yaml
├── prompts/
│   ├── implement.md
│   ├── verify.md
│   └── change-request.md
└── application/
    └── .gitkeep
```

## Folder Purpose

-   `specs/` contains the specification artifacts that define what the
    system must do.
-   `AGENTS.md` tells the AI coding agent how to work with those
    specifications.
-   `prompts/implement.md` triggers the first implementation.
-   `prompts/verify.md` verifies the generated implementation against
    the specification.
-   `prompts/change-request.md` is used when a requirement changes after
    implementation.
-   `application/` is intentionally empty at the start. The AI coding
    agent generates the Spring Boot application here.

## Tutorial Workflow

Requirements → System Specification → Acceptance Criteria → Technical
Constraints → OpenAPI Contract → AGENTS.md → Implementation Prompt →
Agent Plan → Generate `/application` → Tests → Verification

> The `.gitkeep` file exists only so Git can preserve the initially
> empty `application/` directory.




## Running the Project with Codex
Run all commands from the root of the tutorial repository.

### 1. Open the Tutorial Directory
```bash
cd sdd-series-tutorial-01
```

### 2. Start Codex
If Codex is not installed globally:

```bash
npx @openai/codex
```

If Codex is already installed:
```bash
codex
```
---

## Implement from the Specification
The implementation prompt is stored in:
```text
prompts/implement.md
```
Run:
```bash
npx @openai/codex "$(cat prompts/implement.md)"
```

Or, if Codex is installed globally:
```bash
codex "$(cat prompts/implement.md)"
```

Codex should:
1. Read `AGENTS.md`.
2. Read all specification files under `specs/`.
3. Create an implementation plan.
4. Generate the Spring Boot application inside `application/`.
5. Generate automated tests.
6. Run the test suite.
7. Fix implementation issues without modifying the specifications.

---

## Verify the Generated Application
After implementation, run the verification prompt:

```bash
npx @openai/codex "$(cat prompts/verify.md)"
```

Or:

```bash
codex "$(cat prompts/verify.md)"
```

The verification step checks the implementation against:
- Business requirements
- System specification
- Acceptance criteria
- Technical constraints
- OpenAPI contract
- Automated tests

---
## Handle a Requirement Change
When an existing business requirement changes, use:

```bash
npx @openai/codex "$(cat prompts/change-request.md)"
```

Or:

```bash
codex "$(cat prompts/change-request.md)"
```

The expected workflow is:
```text
Requirement Change
        ↓
Update Specification
        ↓
Impact Analysis
        ↓
Review Plan
        ↓
Update Implementation
        ↓
Update Tests
        ↓
Run Complete Test Suite
        ↓
Verify Against Specification
```

---
## Useful Codex Commands
Start Codex interactively:

```bash
npx @openai/codex
```

Start Codex using the implementation instructions:
```bash
npx @openai/codex "$(cat prompts/implement.md)"
```

Verify the implementation:
```bash
npx @openai/codex "$(cat prompts/verify.md)"
```

Process a requirement change:
```bash
npx @openai/codex "$(cat prompts/change-request.md)"
```

---
## SDD Workflow
```text
Business Requirements
        ↓
System Specification
        ↓
Acceptance Criteria
        ↓
Technical Constraints
        ↓
OpenAPI Contract
        ↓
AGENTS.md
        ↓
Implementation Prompt
        ↓
Codex
        ↓
Implementation Plan
        ↓
Generate /application
        ↓
Automated Tests
        ↓
Verification
```

> The specifications are the source of truth. If the implementation conflicts with the specification, fix the implementation rather than changing the specification simply to make the code pass.
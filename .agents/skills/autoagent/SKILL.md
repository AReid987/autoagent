```markdown
# autoagent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `autoagent` TypeScript codebase. You will learn the project's file naming, import/export styles, commit patterns, and how to write and run tests. This guide is ideal for contributors seeking to maintain consistency and best practices in the repository.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myUtility.ts`, `userAgentManager.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { fetchData } from './networkUtils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In userAgentManager.ts
    export function createAgent() { ... }
    export const AGENT_VERSION = '1.0.0';

    // In another file
    import { createAgent, AGENT_VERSION } from './userAgentManager';
    ```

### Commit Patterns
- Commits are **freeform** (no enforced prefixes).
- Average commit message length: **62 characters**.
  - Example:
    ```
    Improve agent initialization logic for better performance
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add new functionality.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Implement your logic using TypeScript.
3. Use relative imports to bring in dependencies.
4. Export your functions or constants using named exports.
5. Add or update corresponding test files (e.g., `newFeature.test.ts`).
6. Commit your changes with a clear, descriptive message.

### Writing and Running Tests
**Trigger:** When you add or modify code.
**Command:** `/run-tests`

1. Create or update test files matching the pattern `*.test.*` (e.g., `userAgentManager.test.ts`).
2. Write your tests using the project's (unknown) test framework.
3. Run the test suite using the appropriate command for your environment (e.g., `npm test` or `yarn test`).

## Testing Patterns

- Test files follow the pattern: `*.test.*`
  - Example: `networkUtils.test.ts`
- The specific testing framework is **unknown**; refer to existing test files for structure.
- Place tests alongside or near the modules they test.

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /add-module  | Scaffold a new module with conventions  |
| /run-tests   | Run the test suite                      |
```
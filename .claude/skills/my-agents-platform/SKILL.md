```markdown
# my-agents-platform Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to the development patterns and conventions used in the `my-agents-platform` TypeScript codebase. It covers file and code style conventions, commit patterns, and testing practices to ensure consistency and maintainability across the project. While no specific frameworks or automated workflows were detected, this guide will help you align with the established standards and streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - **Example:** `agentManager.ts`, `userProfile.test.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - **Example:**
    ```typescript
    import { Agent } from './agentManager';
    ```

### Export Style
- Use **named exports** for all modules.
  - **Example:**
    ```typescript
    // agentManager.ts
    export function createAgent() { ... }
    export const AGENT_TYPE = 'basic';
    ```

### Commit Patterns
- Follow **Conventional Commits** with the `build` prefix.
  - **Example:**  
    ```
    build: update dependencies for agent module
    ```

## Workflows

_No automated workflows were detected in this repository. However, here are suggested manual workflows based on common development tasks:_

### Code Development
**Trigger:** When adding or updating features or modules  
**Command:** `/dev`

1. Create or update TypeScript files using camelCase naming.
2. Use relative imports and named exports.
3. Write clear, conventional commit messages (e.g., `build: add new agent feature`).
4. Add corresponding test files with the `.test.ts` suffix.

### Testing
**Trigger:** When validating code changes  
**Command:** `/test`

1. Locate or create test files matching `*.test.ts`.
2. Run your preferred test runner (e.g., `ts-node`, `jest`, or similar).
3. Ensure all tests pass before committing changes.

### Code Review
**Trigger:** Before merging code into the main branch  
**Command:** `/review`

1. Check that all code follows the documented conventions.
2. Verify that all new or changed code is covered by tests.
3. Confirm that commit messages use the correct conventional format.

## Testing Patterns

- Test files should follow the `*.test.ts` naming pattern.
- Place test files alongside the modules they test or in a dedicated test directory.
- The specific testing framework is not defined; choose one compatible with TypeScript (e.g., Jest, Mocha).
- Example test file:
  ```typescript
  // agentManager.test.ts
  import { createAgent } from './agentManager';

  describe('createAgent', () => {
    it('should create a new agent', () => {
      const agent = createAgent();
      expect(agent).toBeDefined();
    });
  });
  ```

## Commands
| Command   | Purpose                                  |
|-----------|------------------------------------------|
| /dev      | Start or update development on a feature |
| /test     | Run all tests                            |
| /review   | Perform code review before merging       |
```
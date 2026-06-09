```markdown
# my-agents-platform Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to the development patterns, coding conventions, and workflows used in the `my-agents-platform` TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns, equipping contributors with the knowledge to maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `agentManager.ts`, `userProfile.ts`

### Import Style
- Use **relative imports** for referencing modules within the codebase.
  - Example:
    ```typescript
    import { Agent } from './agentManager';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // agentManager.ts
    export function createAgent() { ... }
    export const AGENT_STATUS = { ... };
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use the `build` prefix for build-related changes.
- Keep commit messages concise (average ~75 characters).
  - Example:
    ```
    build: update dependencies to latest stable versions
    ```

## Workflows

### Build Workflow
**Trigger:** When preparing the project for deployment or after making changes to dependencies.
**Command:** `/build`

1. Ensure all dependencies are up to date.
2. Run the build script (typically `npm run build` or equivalent).
3. Verify the output for errors or warnings.
4. Commit changes with a `build:` prefix in the commit message.

   Example:
   ```
   build: compile TypeScript sources and update dist files
   ```

## Testing Patterns

- Test files are named with the pattern `*.test.*` (e.g., `agentManager.test.ts`).
- The specific testing framework is not detected; check project documentation or existing test files for details.
- To add a test:
  1. Create a new file following the `*.test.ts` pattern.
  2. Use relative imports to bring in the module under test.
  3. Use named exports for test utilities and helpers.

  Example:
  ```typescript
  // agentManager.test.ts
  import { createAgent } from './agentManager';

  describe('createAgent', () => {
    it('should create an agent with default properties', () => {
      const agent = createAgent();
      expect(agent).toHaveProperty('id');
    });
  });
  ```

## Commands
| Command   | Purpose                                      |
|-----------|----------------------------------------------|
| /build    | Run the build process for the project        |
```

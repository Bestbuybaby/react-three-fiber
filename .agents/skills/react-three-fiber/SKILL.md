```markdown
# react-three-fiber Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the development patterns and conventions used in the `react-three-fiber` codebase, a TypeScript project built on top of React. You'll learn how to structure files, write imports/exports, follow commit message conventions, and understand the project's approach to testing.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myComponent.tsx`, `useCustomHook.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { useThree } from './useThree'
    import { Canvas } from '../core/Canvas'
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    export function useCustomHook() { ... }
    export const MyComponent = () => { ... }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Common prefix: `chore`
- Example:
  ```
  chore: update dependencies to latest versions
  ```

## Workflows

### Code Contribution
**Trigger:** When adding new features, bug fixes, or improvements  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write code using camelCase file names and relative imports.
3. Use named exports for all modules.
4. Write or update tests in files matching `*.test.*`.
5. Commit changes using the conventional commit format (e.g., `chore: ...`).
6. Push your branch and open a pull request.

### Running Tests
**Trigger:** Before submitting code or verifying changes  
**Command:** `/run-tests`

1. Locate test files matching the pattern `*.test.*`.
2. Run the project's test runner (framework unknown; typically `npm test` or `yarn test`).
3. Ensure all tests pass before committing.

### Code Review
**Trigger:** When reviewing a pull request  
**Command:** `/review`

1. Check that file naming and import/export conventions are followed.
2. Verify commit messages use the conventional format.
3. Ensure tests exist and pass for new or changed code.
4. Leave feedback or approve the pull request.

## Testing Patterns

- Test files use the pattern `*.test.*` (e.g., `myComponent.test.tsx`).
- The specific testing framework is not specified.
- Place tests alongside the code or in a dedicated test directory.
- Example test file:
  ```typescript
  // myComponent.test.tsx
  import { render } from '@testing-library/react'
  import { MyComponent } from './myComponent'

  test('renders correctly', () => {
    const { getByText } = render(<MyComponent />)
    expect(getByText('Hello')).toBeInTheDocument()
  })
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /contribute    | Steps to contribute new code                 |
| /run-tests     | How to run and verify tests                  |
| /review        | Checklist for code review and best practices |
```
```markdown
# examples-NGshiyu Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `examples-NGshiyu` Java repository. It covers file organization, code style, commit practices, and testing patterns to help contributors maintain consistency and quality.

## Coding Conventions

### File Naming
- **Pattern:** PascalCase
- **Example:**  
  ```java
  public class UserProfile { ... }
  ```

### Import Style
- **Pattern:** Relative imports
- **Example:**  
  ```java
  import mypackage.utils.StringHelper;
  ```

### Export Style
- **Pattern:** Named exports (Java public classes/methods)
- **Example:**  
  ```java
  public class DataProcessor {
      public static void process() { ... }
  }
  ```

### Commit Messages
- **Pattern:** Conventional commits with `feat` prefix
- **Example:**  
  ```
  feat: add user authentication module
  ```

## Workflows

### Feature Development
**Trigger:** When implementing a new feature  
**Command:** `/feature-dev`

1. Create a new branch for the feature.
2. Use PascalCase for new file/class names.
3. Use relative imports for dependencies.
4. Write clear, conventional commit messages with the `feat` prefix.
5. If applicable, add or update corresponding test files (`*.test.*`).

### Code Review Preparation
**Trigger:** Before submitting a pull request  
**Command:** `/prepare-review`

1. Ensure all new files follow PascalCase naming.
2. Check that all imports are relative.
3. Confirm that all exports are named (public classes/methods).
4. Run all tests (see Testing Patterns).
5. Review commit messages for correct format.

### Testing
**Trigger:** Before merging or after writing new code  
**Command:** `/run-tests`

1. Locate test files matching the pattern `*.test.*`.
2. Run tests using the project's preferred method (framework unknown; check project documentation or use standard Java test runners).
3. Ensure all tests pass before proceeding.

## Testing Patterns

- **File Pattern:** Test files are named with the pattern `*.test.*` (e.g., `UserService.test.java`).
- **Framework:** Not explicitly specified; use standard Java testing practices (e.g., JUnit).
- **Example:**
  ```java
  public class UserServiceTest {
      @Test
      public void testUserCreation() {
          // test logic here
      }
  }
  ```

## Commands
| Command         | Purpose                                    |
|-----------------|--------------------------------------------|
| /feature-dev    | Start a new feature development workflow    |
| /prepare-review | Prepare code for review and pull request    |
| /run-tests      | Run all tests in the repository             |
```
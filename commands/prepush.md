---
description: Pre-push code verification against origin/develop - checks for code quality, DRY/SOLID principles, and removes unnecessary code
argument-hint: [optional: specific files or paths]
---

# Pre-Push Code Verification

Perform a comprehensive code quality check against origin/develop before pushing changes.

## Tasks to Complete

1. **Fetch Latest Changes**
   - Fetch origin/develop to ensure comparison against latest code
   - Show summary of changed files compared to origin/develop

2. **Analyze Changed Code**
   - Get list of all modified files compared to origin/develop
   - Review each changed file for:
     - Unnecessary comments (commented-out code, outdated TODOs)
     - Code duplication and DRY violations
     - SOLID principle violations
     - Dead code or unused imports/variables
     - Test files that should be removed
     - Legacy code that's no longer used

3. **Specific Checks**
   - **Comments**: Remove:
     - Commented-out code blocks
     - Outdated or redundant comments
     - Debug console.log statements
   - **DRY (Don't Repeat Yourself)**:
     - Identify duplicate code blocks
     - Suggest extracting common patterns into shared functions/utilities
   - **SOLID Principles**:
     - Single Responsibility: Functions/classes doing too many things
     - Open/Closed: Hard-coded values that should be configurable
     - Liskov Substitution: Inheritance issues
     - Interface Segregation: Overly complex interfaces
     - Dependency Inversion: Direct dependencies that should be injected
   - **Dead Code**:
     - Unused imports, variables, functions
     - Unreachable code paths
     - Test files in non-test directories
     - Legacy files no longer referenced

4. **Report & Fix**
   - Generate a summary report of all issues found
   - For each issue, provide:
     - File path and line number
     - Issue type (comment/DRY/SOLID/dead code)
     - Specific problem description
     - Suggested fix
   - Ask for confirmation before applying fixes
   - Apply approved fixes
   - Re-run linter and type checker

5. **Final Verification**
   - Show git diff of all fixes applied
   - Confirm all changes are intentional
   - Run `yarn lint` and `yarn build` to ensure no breakage

## Arguments
- If `$ARGUMENTS` is provided, focus analysis only on those specific files/paths
- If no arguments, analyze all files changed compared to origin/develop

## Output Format
Provide a structured report with:
- Total files analyzed
- Issues found by category
- Detailed findings with file:line references
- Applied fixes summary
- Final verification status

Let's ensure the code is clean, maintainable, and follows best practices before pushing! 🔔

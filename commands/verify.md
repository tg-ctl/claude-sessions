---
description: Verify implementation completeness and quality for an issue
argument-hint: <issue_number>
---

# Verify Issue Implementation

Comprehensive verification of completed work against issue requirements and PLAN.md.

## Required Argument
- `$1`: Issue number (e.g., 255, 261)

## Process

1. **Load Context**
   - Read `issues/$1/README.md` for requirements
   - Read `issues/$1/PLAN.md` for expected implementation
   - Get list of files changed in current branch vs origin/develop
   - Identify files related to this issue

2. **Requirements Verification**
   - Check each requirement from README.md
   - Verify acceptance criteria are met
   - Confirm all planned features are implemented
   - Cross-reference PLAN.md tasks with actual changes

3. **Code Quality Checks**
   - **Linting**: Run `yarn lint` on changed files
   - **Type Safety**: Run `yarn build` to check TypeScript errors
   - **Code Style**: Verify follows project conventions
   - **Patterns**: Check Angular/NestJS patterns from CLAUDE.md
   - **Dependencies**: Verify no unauthorized libraries added

4. **Implementation Review**
   For each changed file:
   - **Purpose**: Does it align with issue goals?
   - **Completeness**: All necessary changes present?
   - **DRY**: No duplicate code introduced?
   - **SOLID**: Follows design principles?
   - **Comments**: Only necessary comments, no dead code?
   - **Tests**: Test files removed from non-test directories?
   - **Imports**: No unused imports?
   - **Console logs**: No debug statements left?

5. **Database & Migrations**
   - If migrations added: verify naming, rollback, no test data
   - Check model relations and mixins are correct
   - Verify migrations run successfully

6. **Integration Checks**
   - API routes follow `/-/api/**` pattern?
   - Permissions use `@UserCan()` decorators?
   - Feature toggles use `@RequireFeatures()`?
   - Forms use Angular Reactive Forms pattern?
   - State management follows service-based architecture?

7. **Testing**
   - Run `yarn test` if tests exist
   - Verify test coverage for new features
   - Manual testing checklist from PLAN.md

8. **Git Hygiene**
   - Run `git status` to check uncommitted changes
   - Review `git diff origin/develop` for unintended changes
   - Verify commit messages if already committed
   - Check no sensitive data or secrets exposed

9. **Documentation**
   - Code is self-documenting or has necessary comments
   - Complex logic is explained
   - API endpoints documented if applicable

10. **Generate Verification Report**
    Create `issues/$1/VERIFICATION.md` with:
    - ✅ Requirements met / ❌ Requirements missing
    - ✅ Quality checks passed / ⚠️ Issues found
    - 📝 List of all files changed
    - 🔍 Detailed findings by category
    - 📊 Summary: Ready to push? Yes/No
    - 🛠️ Action items if issues found

11. **Final Assessment**
    - Show verification summary
    - Highlight any blockers or issues
    - Provide recommendations
    - Update issue status if fully verified
    - Ring bell if ready to push 🔔

## Example Usage
```
/verify 261
```

## Output
- Comprehensive verification report
- Saved to `issues/$1/VERIFICATION.md`
- Clear pass/fail status for each check
- Actionable items if issues found
- Ready-to-push confirmation or fixes needed

Let's ensure the implementation meets all requirements and quality standards! ✅

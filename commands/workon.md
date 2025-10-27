---
description: Execute implementation of issue based on PLAN.md
argument-hint: <issue_number>
---

# Work On Issue

Execute the implementation of an issue following its detailed PLAN.md.

## Required Argument
- `$1`: Issue number (e.g., 255, 261)

## Prerequisites
- `issues/$1/PLAN.md` must exist (use `/issue $1` first if not)

## Process

1. **Load Plan & Setup**
   - Read `issues/$1/PLAN.md`
   - Read `issues/$1/README.md` for issue context
   - Update issue status to WIP
   - Create TodoWrite task list from PLAN.md implementation steps

2. **Execute Plan Systematically**
   - Follow PLAN.md steps in order
   - Mark each task as in_progress when starting
   - Complete one task at a time
   - Mark tasks completed immediately after finishing
   - Update todo list in real-time

3. **Implementation Standards**
   - Follow existing code conventions
   - Read files before editing
   - Prefer editing over creating new files
   - Use existing libraries (check package.json)
   - Apply proper TypeScript types
   - Follow Angular/NestJS patterns from CLAUDE.md

4. **Verification After Each Step**
   - Run `yarn lint` after code changes
   - Run `yarn build` to check for type errors
   - Test functionality if applicable
   - Verify changes match plan requirements

5. **Progress Tracking**
   - Keep todo list synchronized with actual progress
   - Note any deviations from plan with reasons
   - Document blockers or issues encountered
   - Update PLAN.md if approach changes

6. **Completion**
   - Final verification: lint + build + tests
   - Review all changes against issue requirements
   - Show git diff summary
   - Update issue status to Done
   - Ask if ready to commit changes
   - Ring bell 🔔

## Key Principles
- **Stay focused**: Only do what's in PLAN.md
- **One task at a time**: Complete before moving to next
- **Real-time updates**: TodoWrite reflects current state
- **Verify continuously**: Don't wait until end to test
- **Follow the plan**: Deviate only when necessary

## Example Usage
```
/workon 261
```

## Output
- Task-by-task execution following PLAN.md
- Real-time progress via TodoWrite
- Verification results after each step
- Final summary of all changes made

Let's execute the plan efficiently and systematically! 🚀

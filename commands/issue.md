---
description: Analyze issue and create detailed implementation plan with ultrathinking
argument-hint: <issue_number>
---

# Issue Analysis & Planning

Analyze the specified issue and create a comprehensive implementation plan using deep thinking.

## Required Argument
- `$1`: Issue number (e.g., 255, 261)

## Process

1. **Load Issue Context**
   - Read `issues/$1/README.md` or main issue file
   - Parse issue description, requirements, and acceptance criteria
   - Identify related files mentioned in the issue
   - Check for existing work-in-progress files

2. **Deep Analysis with Sequential Thinking**
   - Use the sequential thinking tool to:
     - Break down the problem into components
     - Identify dependencies and prerequisites
     - Consider edge cases and potential challenges
     - Explore multiple solution approaches
     - Evaluate trade-offs and best practices
     - Map out implementation steps
     - Identify testing requirements
     - Consider integration points with existing code

3. **Code Context Discovery**
   - Search codebase for related functionality
   - Identify affected files and modules
   - Review existing patterns and conventions
   - Check related issues or PRs
   - Understand database schema requirements (if applicable)

4. **Create Detailed Plan**
   Generate a comprehensive plan including:
   - **Problem Summary**: Clear description of what needs to be done
   - **Technical Analysis**: Deep dive from sequential thinking
   - **Implementation Steps**: Numbered, actionable tasks
   - **Files to Create/Modify**: Specific file paths
   - **Dependencies**: Libraries, migrations, related issues
   - **Testing Strategy**: Unit tests, integration tests, manual testing
   - **Risks & Considerations**: Potential issues and mitigations
   - **Estimated Complexity**: Time/effort estimate

5. **Save Plan**
   - Create `issues/$1/PLAN.md` with the detailed plan
   - Include思考 process insights from sequential thinking
   - Add file references with line numbers where applicable
   - Format with clear sections and markdown

6. **Ready to Execute**
   - Update `issues/$1/README.md` status to WIP if starting
   - Provide summary of plan
   - Ask if ready to begin implementation

## Example Usage
```
/issue 261
```

## Output
- Comprehensive analysis using sequential thinking
- Detailed plan saved to `issues/$1/PLAN.md`
- Summary of approach and next steps
- Ready-to-execute task breakdown

Let's think deeply about the issue and create a solid plan! 🧠

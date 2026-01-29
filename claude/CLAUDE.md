# Project Instructions for Claude AI

## Project Context

This project uses AI-assisted development with a focus on quality, maintainability, and structured problem-solving. The guidelines below should inform all code generation, analysis, and recommendations.

## Core Principles

### Code Quality
- Prioritize simple, readable code with minimal abstraction
- Avoid premature optimization
- Write pure functions when possible (do not mutate inputs; only return new values)
- Keep functions focused and single-purpose
- Document complex logic with clear comments

### Development Workflow
- Follow established patterns and architecture
- Update documentation when making changes
- Maintain the Memory Bank for persistent context
- Use structured problem-solving approaches
- Validate changes through testing

## Quality Tools & Methodologies

Apply these quality tools from Six Sigma and Lean to software engineering:

### Root Cause Analysis
- **5 Whys**: Iteratively ask "Why?" to drill down to root causes
- **Fishbone Diagram**: Categorize possible causes (People, Methods, Machines, Materials, Measurements, Environment)
- **Root Cause Verification**: Verify suspected causes before implementing fixes

### Continuous Improvement
- **PDCA Cycle**: Plan → Do → Check → Act for testing and implementing fixes
- **Pareto Analysis**: Identify and prioritize the most impactful issues
- **FMEA**: For critical systems, identify failure points and rank risks

### Problem-Solving Approach
1. Define the problem clearly with measurable impact
2. Understand the process and identify where issues occur
3. Analyze root causes using appropriate tools
4. Prioritize and plan solutions
5. Test and verify fixes
6. Document learnings and prevent recurrence

## Memory Bank Structure

The Memory Bank is crucial for maintaining context between sessions. It consists of:

### Core Files
1. **projectbrief.md** - Foundation document defining core requirements and goals
2. **productContext.md** - Why the project exists, problems it solves, user experience goals
3. **activeContext.md** - Current work focus, recent changes, next steps, active decisions
4. **systemPatterns.md** - System architecture, key technical decisions, design patterns
5. **techContext.md** - Technologies used, development setup, technical constraints
6. **progress.md** - What works, what's left to build, current status, known issues

### Workflow
- Read ALL memory bank files at the start of EVERY task
- Update when discovering new patterns or after implementing significant changes
- Document current state and clarify next steps
- Focus particularly on activeContext.md and progress.md for current state

## Technical Specifications

When writing technical specifications:

### Language Usage
- Use "**Shall**" for requirements (obligatory statements)
- Use "**Will**" for facts or declarations of purpose
- Use "**Should**" for goals

### Requirements Quality
- Be clear, concise, and unambiguous
- Express only one thought per statement
- State requirements as completely as possible
- Minimize "To Be Determined" (TBD) values
- Ensure consistency with other requirements
- Maintain bidirectional traceability
- Include quantifiable values and tolerances where applicable

### Documentation Structure
- Architecture Design Baseline
- System Element Detailed Descriptions
- Requirements Assigned to System Elements
- Interface Requirements
- Verification Strategy and Plans
- End-Product Specifications

## Feature Development

### Planning Process
1. Analyze the codebase to understand relevant sections and architecture
2. Review existing coding patterns
3. Identify the area where the solution will be implemented
4. Break down into logical, sequential sprints
5. Document approach in `/docs/features/{feature-name}/`

### Sprint Planning Structure
```
# {Feature Title} Plan

## Overview
{Executive summary of the feature}

## Business Value and Objectives
{How this feature adds value}

## Codebase Review
### Background
{Description of the implementation area}

### Relevant Code
{Files, documentation, integrations, data structures with full paths}

## Implementation Approach
{Logical, sequential sprints with clear descriptions}
```

## Bug Fixing Process

1. Follow guidelines in the ai_instructions.md
2. Visit memory bank and project documentation in /docs folder
3. Analyze the error/issues and identify root cause
4. Identify which files need to be modified
5. Create at least two ways to solve the problem
6. For major changes, present overview and analysis before proceeding
7. Keep solutions simple and in scope
8. Update memory bank and documentation when finished

### Major Changes Requiring Approval
- New/old packages
- New files
- Big changes from existing architecture
- New interfaces
- Changes to database or API

## Commands & Prompts

Reference the commands in the `/commands` folder for structured approaches to:
- Root cause analysis (/rca)
- 5 Whys analysis (/5whys)
- Fishbone diagrams (/fishbone)
- Agile planning (/createAgilePlan)
- Sprint creation (/createAgileSprint)
- Problem-solving frameworks

## Documentation Requirements

When completing work:
1. Update relevant documentation in /docs folder
2. Update memory bank with new learnings
3. Create task lists with checkboxes for tracking
4. Document any improvements discovered
5. Ensure bidirectional traceability

## Testing & Validation

- Write tests that align with existing test infrastructure
- Validate changes before considering work complete
- Run relevant linters and build processes
- Test edge cases
- Ensure no regression in existing functionality

## MCP Connections

Utilize available Model Context Protocol (MCP) connections when appropriate for:
- External integrations
- Data retrieval
- Tool interactions
- Enhanced capabilities

---

**Remember**: Treat every coding issue as a process problem. Use structured thinking and data wherever possible, instead of guesswork.

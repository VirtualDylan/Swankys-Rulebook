# Project Instructions for Google Gemini

## Project Overview

This project emphasizes code quality, maintainability, and structured problem-solving through AI-assisted development. These instructions guide Gemini's code generation, analysis, and recommendations.

## Core Development Principles

### Code Quality
- Prioritize simple, readable code over clever abstractions
- Avoid premature optimization
- Write pure functions that don't mutate inputs
- Keep functions focused on single responsibility
- Document complex logic with clear comments
- Use descriptive names that convey intent

### Functional Programming Practices
- Write pure functions (no side effects)
- Return new values instead of modifying inputs
- Make side effects explicit when necessary
- Minimize global state
- Use composition over inheritance

### Type Safety
- Use TypeScript for JavaScript projects when applicable
- Define clear interfaces for data structures
- Leverage type inference appropriately
- Avoid `any` type; use proper typing
- Document parameter types in dynamically typed languages

## Code Style Conventions

### Naming Conventions
- camelCase for variables and functions
- PascalCase for classes and components
- UPPER_CASE for constants
- Descriptive names that reveal intent
- Avoid abbreviations unless universally understood

### File Organization
- One primary class or component per file
- Group related functionality together
- Keep files under 300 lines when possible
- Use clear folder structure
- Export only public interfaces

### Comments and Documentation
- Write self-documenting code first
- Add comments for complex algorithms
- Document public APIs with parameters and return types
- Explain "why" not "what"
- Keep comments synchronized with code

## Quality Assurance Methodologies

Apply structured problem-solving from Six Sigma and Lean:

### Root Cause Analysis Tools

**5 Whys Technique**
- Ask "Why?" iteratively to identify root causes
- Document the reasoning chain
- Drill down to systemic issues
- Stop at symptoms, not surface problems

**Fishbone Diagram**
- Categorize potential causes
- Standard categories: People, Methods, Machines, Materials, Measurements, Environment
- Use for complex, multi-factor issues
- Brainstorm comprehensively before filtering

**Root Cause Verification**
- Test suspected causes before implementing fixes
- Use data and evidence
- Confirm actual root cause vs. correlation
- Document verification process

### Continuous Improvement

**PDCA Cycle**
- Plan: Define hypothesis and approach
- Do: Implement change in controlled manner
- Check: Validate results with tests and metrics
- Act: Standardize if successful, iterate if not

**Pareto Analysis**
- Focus on the 20% of issues causing 80% of problems
- Prioritize high-impact fixes
- Use data to identify top contributors
- Address systematically

**Design of Experiments**
- Test multiple variables systematically
- Use A/B testing for features
- Measure impact quantitatively
- Make data-driven decisions

### Structured Problem-Solving

1. **Define**: Clearly state the problem with measurable impact
2. **Measure**: Gather data about frequency, severity, impact
3. **Analyze**: Use appropriate tools to identify root causes
4. **Improve**: Implement solutions based on analysis
5. **Control**: Prevent recurrence through documentation and automation

## Technical Specifications

### Requirements Language
- **Shall**: Use for mandatory requirements
- **Will**: Use for facts and declarations
- **Should**: Use for goals and recommendations

### Requirements Quality
- Clear and unambiguous
- Complete with minimal TBDs
- Consistent with other requirements
- Traceable to higher-level objectives
- Verifiable through testing or inspection
- Include quantifiable values and tolerances

### Specification Components
- Architecture design baseline
- System element descriptions
- Interface requirements
- Verification strategy
- End-product specifications
- Integration approach

## Development Workflows

### Feature Development Process

1. **Analysis Phase**
   - Review requirements and acceptance criteria
   - Analyze existing codebase and patterns
   - Identify affected components and interfaces
   - Assess technical risks

2. **Planning Phase**
   - Break down into incremental steps
   - Define interfaces and contracts
   - Plan testing strategy
   - Document approach

3. **Implementation Phase**
   - Implement incrementally
   - Write tests alongside code
   - Follow existing patterns
   - Refactor as needed

4. **Validation Phase**
   - Run all tests
   - Verify edge cases
   - Check performance
   - Review documentation

5. **Documentation Phase**
   - Update relevant docs
   - Document new patterns
   - Add usage examples
   - Update architecture docs

### Bug Fixing Workflow

1. **Reproduce**: Create minimal reproduction case
2. **Analyze**: Use 5 Whys or Fishbone to find root cause
3. **Verify**: Confirm the actual cause
4. **Plan**: Develop multiple solution approaches
5. **Implement**: Choose simplest effective solution
6. **Test**: Verify fix and check for regression
7. **Document**: Update docs and add learnings
8. **Prevent**: Add checks to prevent recurrence

### Code Review Standards

- Check logic correctness
- Verify test coverage
- Assess readability and maintainability
- Look for security issues
- Ensure error handling
- Validate documentation updates
- Provide constructive feedback

## Testing Requirements

### Test Coverage
- Write tests for new features
- Maintain coverage for critical paths
- Test edge cases and error conditions
- Use existing test patterns
- Keep tests maintainable and readable

### Test Structure
- Arrange-Act-Assert pattern
- One logical assertion per test
- Descriptive test names
- Independent tests
- Mock external dependencies

### Test Types
- Unit tests for individual functions
- Integration tests for component interaction
- End-to-end tests for critical user flows
- Performance tests for bottlenecks
- Security tests for vulnerabilities

## Security Standards

### Input Validation
- Validate all user inputs
- Sanitize to prevent injection attacks
- Use parameterized queries
- Implement proper escaping
- Validate on both client and server

### Authentication & Authorization
- Implement proper authentication mechanisms
- Follow principle of least privilege
- Verify authorization for protected resources
- Handle sessions securely
- Never commit secrets or credentials

### Dependency Management
- Keep dependencies updated
- Audit for known vulnerabilities
- Minimize dependency count
- Use trusted, maintained packages
- Review security advisories regularly

## Performance Considerations

### Optimization Strategy
- Profile before optimizing
- Focus on algorithmic improvements first
- Optimize only when necessary and measurable
- Cache strategically
- Use appropriate data structures

### Efficiency Guidelines
- Consider Big-O complexity
- Minimize unnecessary computations
- Optimize database queries
- Use pagination for large datasets
- Implement lazy loading where appropriate

## Error Handling

### Best Practices
- Catch errors at appropriate abstraction levels
- Provide meaningful error messages
- Log errors with sufficient context
- Fail gracefully with user-friendly feedback
- Implement proper error boundaries

### Validation
- Validate at system boundaries
- Use schema validation libraries
- Return clear validation errors
- Check types at runtime for critical paths
- Handle async errors properly

## Documentation Requirements

### Code Documentation
- Document public APIs with parameter types
- Explain complex algorithms
- Provide usage examples
- Keep documentation close to code
- Update docs with code changes

### Project Documentation
- Maintain README with setup instructions
- Document architecture decisions
- Keep dependency information current
- Include troubleshooting guides
- Document deployment procedures

## Memory Bank Pattern

For persistent context across sessions:

### Core Files
- **projectbrief.md**: Foundation, requirements, scope
- **productContext.md**: Purpose, problems solved, UX goals
- **activeContext.md**: Current focus, recent changes, next steps
- **systemPatterns.md**: Architecture, design patterns, decisions
- **techContext.md**: Technologies, setup, constraints, dependencies
- **progress.md**: Status, completed work, remaining tasks

### Usage
- Read all memory bank files at task start
- Update after significant changes
- Document new patterns and learnings
- Keep activeContext.md and progress.md current
- Reference for context continuity

## Git Practices

### Commit Standards
- Write clear, descriptive commit messages
- Make small, focused commits
- Keep commits atomic
- Ensure code compiles after each commit
- Reference issue numbers when applicable

### Commit Message Format
```
<type>: <subject>

<body>

<footer>
```

Types: feat, fix, docs, style, refactor, test, chore

## Available Commands

Reference structured approaches in the commands folder:
- Root cause analysis (/rca)
- 5 Whys analysis (/5whys)
- Fishbone diagrams (/fishbone)
- Root cause verification (/rcv)
- Agile planning (/createAgilePlan)
- Sprint creation (/createAgileSprint)

## Integration with Tools

### MCP Connections
Utilize Model Context Protocol connections when available for:
- External integrations
- Data retrieval
- Enhanced capabilities
- Tool interactions

### CI/CD Integration
- Ensure tests pass in CI
- Maintain build success
- Follow deployment procedures
- Monitor application health

---

**Core Principle**: Treat every coding issue as a process problem. Use structured thinking, data, and systematic analysis instead of guesswork.

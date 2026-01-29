# GitHub Copilot Instructions

## Project Overview

This project emphasizes code quality, maintainability, and structured problem-solving. Use these instructions to guide code generation, suggestions, and reviews.

## Code Quality Standards

### Clarity and Simplicity
- Prioritize readable, simple code over clever abstractions
- Avoid premature optimization
- Use clear, descriptive names for variables, functions, and classes
- Keep functions focused on a single responsibility
- Limit function length to maintain readability

### Functional Programming
- Write pure functions that don't mutate inputs
- Return new values instead of modifying existing ones
- Minimize side effects
- Make side effects explicit and contained

### Type Safety
- Use TypeScript for type safety where applicable
- Define clear interfaces for data structures
- Avoid `any` type; use proper typing
- Leverage type inference when it improves readability

## Code Style Conventions

### Naming
- Use camelCase for variables and functions
- Use PascalCase for classes and components
- Use UPPER_CASE for constants
- Use descriptive names that convey intent
- Avoid single-letter variables except in small loops

### Organization
- Group related functionality together
- Keep files focused on single responsibility
- Use consistent file and folder structure
- Export only what's necessary
- Use index files for clean imports

### Comments
- Write self-documenting code first
- Add comments for complex algorithms
- Document public APIs and interfaces
- Explain "why" not "what"
- Keep comments up-to-date with code

## Testing Requirements

### Test Coverage
- Write tests for new features
- Maintain coverage for critical paths
- Test edge cases and error conditions
- Use existing test patterns and infrastructure
- Ensure tests are readable and maintainable

### Test Structure
- Follow Arrange-Act-Assert pattern
- One assertion concept per test
- Use descriptive test names
- Mock external dependencies
- Keep tests independent

## Architecture Patterns

### Component Design
- Prefer composition over inheritance
- Keep components small and focused
- Use functional components over classes (React)
- Separate presentation from logic
- Make components reusable when appropriate

### State Management
- Keep state as local as possible
- Lift state only when necessary
- Use appropriate state management for scale
- Document complex state flows
- Avoid unnecessary global state

### API Design
- Validate inputs at boundaries
- Return consistent response structures
- Use proper HTTP status codes
- Handle errors gracefully
- Document endpoints and parameters

## Error Handling

### Best Practices
- Catch errors at appropriate levels
- Provide meaningful error messages
- Log errors with sufficient context
- Fail gracefully with user feedback
- Implement proper error boundaries

### Validation
- Validate all user inputs
- Sanitize data to prevent injection
- Use schema validation libraries
- Return clear validation errors
- Check types at runtime for critical paths

## Security Standards

### Input Security
- Validate and sanitize all inputs
- Use parameterized queries for databases
- Prevent SQL injection and XSS
- Implement proper escaping
- Validate on both client and server

### Authentication & Authorization
- Implement proper authentication
- Use principle of least privilege
- Verify authorization for all protected resources
- Handle session management securely
- Don't commit secrets or credentials

### Dependencies
- Keep dependencies updated
- Audit for known vulnerabilities
- Minimize dependency count
- Use trusted, maintained packages
- Review security advisories

## Performance Considerations

### Optimization Strategy
- Optimize only when necessary
- Profile before optimizing
- Focus on algorithmic improvements first
- Cache strategically
- Use lazy loading appropriately

### Efficiency
- Consider Big-O complexity
- Avoid unnecessary re-renders
- Minimize network requests
- Optimize database queries
- Use pagination for large datasets

## Git & Version Control

### Commit Messages
- Use clear, descriptive messages
- Start with verb in imperative mood
- Keep first line under 50 characters
- Add details in body if needed
- Reference issue numbers

### Commit Practices
- Make small, focused commits
- Keep commits atomic
- Ensure code compiles after each commit
- Don't commit commented-out code
- Remove debug statements

## Documentation

### Code Documentation
- Document public APIs
- Explain complex algorithms
- Add usage examples
- Keep documentation close to code
- Update docs with code changes

### Project Documentation
- Maintain README with setup instructions
- Document architecture decisions
- Keep dependency information current
- Include troubleshooting guides
- Document deployment procedures

## Quality Assurance

### Root Cause Analysis
When debugging:
1. Reproduce the issue consistently
2. Identify symptoms vs. root cause
3. Use 5 Whys technique
4. Verify the actual cause
5. Fix root cause, not symptoms

### Problem-Solving Approach
1. Define the problem clearly
2. Gather data and evidence
3. Analyze root causes
4. Generate multiple solutions
5. Choose the simplest effective solution
6. Test thoroughly
7. Document learnings

### Continuous Improvement
- Apply PDCA cycle: Plan-Do-Check-Act
- Learn from bugs and issues
- Share knowledge with team
- Refine processes over time
- Document patterns and anti-patterns

## Workflow Guidelines

### Feature Development
1. Understand requirements fully
2. Review existing code and patterns
3. Plan implementation approach
4. Implement incrementally
5. Write tests alongside code
6. Review and refactor
7. Update documentation

### Bug Fixing
1. Reproduce the bug
2. Identify root cause
3. Create test case for the bug
4. Implement fix
5. Verify fix works
6. Ensure no regression
7. Document the issue and solution

### Code Review
- Review for correctness and style
- Check test coverage
- Verify error handling
- Look for security issues
- Ensure documentation is updated
- Provide constructive feedback

## Commands Reference

Structured approaches for common tasks:
- Root cause analysis
- 5 Whys analysis
- Fishbone diagrams
- Feature planning
- Sprint planning

See the commands folder for detailed templates.

## Tools & Methodologies

Apply quality tools from Six Sigma and Lean:
- 5 Whys for root cause analysis
- Fishbone diagrams for complex issues
- Pareto analysis for prioritization
- PDCA cycle for improvements
- Root cause verification

See QualityTools.md in guidelines for details.

---

**Core Principle**: Treat every coding issue as a process problem. Use structured thinking and data over guesswork.

# GitHub Copilot Instructions

## Setup

### Repository-Wide Instructions

1. Create a `.github` directory in your repository root if it doesn't exist:
   ```bash
   mkdir -p .github
   ```

2. Copy `copilot-instructions.md` to `.github/`:
   ```bash
   cp copilot-instructions.md .github/
   ```

3. Copilot will automatically read and apply these instructions for code generation and reviews

### Path-Specific Instructions (Advanced)

For different rules in different parts of your codebase, create files like:
```
.github/instructions/python.instructions.md
.github/instructions/typescript.instructions.md
```

Add frontmatter to specify which files they apply to:
```markdown
---
applyTo: "*.py"
---

# Python-specific rules here
```

## What's Included

### Main Instructions File
- **copilot-instructions.md** - Repository-wide custom instructions
  - Code quality standards
  - Code style conventions
  - Testing requirements
  - Architecture patterns
  - Error handling guidelines
  - Security standards
  - Performance considerations
  - Git practices
  - Documentation requirements
  - Quality assurance methodologies

### Commands
Structured command templates for common development tasks:
- **5whys.md** - 5 Whys root cause analysis framework
- **createAgilePlan.md** - Comprehensive feature planning template
- **createAgileSprint.md** - Sprint plan generation guide
- **find-rc.md** - Root cause discovery process
- **fishbone.md** - Fishbone diagram analysis method
- **outline.md** - Project outline creation
- **rca.md** - Formal root cause analysis report format
- **rcv.md** - Root cause verification matrix
- **solve-rc.md** - Solution implementation approach

### Guidelines
Reference documentation and detailed methodologies:
- **QualityTools.md** - Six Sigma and Lean quality tools for software engineering
- **TechnicalSpecifications.md** - Guide for writing technical specifications
- **MemoryBank.md** - Persistent documentation patterns for AI-assisted development
- **Fixing a bug.md** - Structured bug fixing workflow
- **New Feature.md** - Feature development process and template
- **New Chat with Directive.md** - Guide for effective AI prompting

## Usage

### Automatic Application

Once the instructions file is in `.github/`, GitHub Copilot automatically:
- Considers instructions when generating code suggestions
- Applies coding standards to autocomplete
- Uses conventions in code reviews
- Maintains consistency across the project

### In VS Code

Copilot uses instructions in:
- **Inline suggestions** - Following code style and patterns
- **Copilot Chat** - Providing contextual assistance
- **Code reviews** - Checking against standards
- **Cmd/Ctrl + I** - Inline chat and edits

### In GitHub

When using Copilot for pull requests:
- Copilot reviews use your instructions
- Suggestions align with project standards
- Comments reference your guidelines

## Best Practices

### Writing Instructions

**Do's:**
- ✅ Be concise and specific
- ✅ Use bullet points for clarity
- ✅ Include code examples
- ✅ Focus on important rules
- ✅ Use clear, actionable language
- ✅ Structure with headings

**Don'ts:**
- ❌ Write overly long instructions
- ❌ Be vague or generic
- ❌ Duplicate standard documentation
- ❌ Include too many edge cases
- ❌ Make rules too restrictive

### Organizing Instructions

**Single File Approach** (Recommended for most projects)
- Keep all instructions in one `.github/copilot-instructions.md`
- Use headings to organize topics
- Limit to most important rules

**Multi-File Approach** (For large/polyglot projects)
- Create `.github/instructions/` directory
- Separate by language or domain
- Use frontmatter for targeting

### Keeping Instructions Current

1. Review instructions quarterly
2. Update when adopting new patterns
3. Remove outdated rules
4. Refine based on Copilot's output quality
5. Solicit feedback from team

## Examples

### Basic Setup
```markdown
# Copilot Instructions

- Use functional components in React
- Prefer const over let
- All functions should have JSDoc comments
- Use Jest for testing
```

### With Code Examples
```markdown
# API Error Handling

Always handle errors with try-catch and return proper status:

\`\`\`typescript
try {
  const result = await apiCall();
  return res.status(200).json(result);
} catch (error) {
  logger.error('API call failed', error);
  return res.status(500).json({ error: 'Internal server error' });
}
\`\`\`
```

### Language-Specific
Create `.github/instructions/python.instructions.md`:
```markdown
---
applyTo: "**/*.py"
---

# Python Standards

- Use type hints for all function parameters
- Follow PEP 8 style guide
- Use pytest for testing
- Document with Google-style docstrings
```

## Integration with Quality Tools

The instructions emphasize structured problem-solving using:

### Root Cause Analysis
- 5 Whys technique for drilling to root causes
- Fishbone diagrams for complex issues
- Root cause verification before fixing

### Continuous Improvement
- PDCA cycle: Plan-Do-Check-Act
- Pareto analysis for prioritization
- Documentation of learnings

See **QualityTools.md** in guidelines for complete methodology.

## Customization

Adapt the instructions for your project:

1. **Language-Specific Rules**
   - Add conventions for your languages
   - Include framework-specific patterns
   - Reference style guides

2. **Project-Specific Standards**
   - Architecture decisions
   - Naming conventions
   - File organization
   - Testing strategies

3. **Team Preferences**
   - Code review criteria
   - Documentation style
   - Git workflow
   - Communication patterns

## Troubleshooting

### Instructions Not Being Applied

**Check:**
- File is in `.github/copilot-instructions.md`
- File has .md extension
- Copilot extension is up to date
- Instructions are clear and specific

**Try:**
- Restart VS Code
- Check file permissions
- Verify GitHub Copilot subscription
- Test with simple, clear rule

### Inconsistent Results

**Solutions:**
- Make rules more specific
- Add code examples
- Use concrete language
- Avoid ambiguous terms
- Provide context for rules

### Performance Issues

**Optimize:**
- Keep instructions under 2000 words
- Focus on most important rules
- Remove redundant content
- Split into targeted files if needed

## Advanced Features

### User-Level Instructions

Set personal preferences across all projects:
1. Open VS Code settings
2. Search for "Copilot"
3. Add user-level instructions
4. These apply when no repo-level instructions exist

### Workspace Instructions

For multi-repo workspaces:
1. Create instructions in workspace root
2. Copilot uses workspace context
3. Can override user-level settings

### Temporary Instructions

In Copilot Chat:
```
@workspace Using React hooks, create a user profile component
```

The `@workspace` tag gives Copilot additional context.

## Monitoring Effectiveness

Track how well instructions work:
1. Review Copilot suggestions quality
2. Note which rules are followed consistently
3. Identify gaps in coverage
4. Collect team feedback
5. Iterate on instructions

## Resources

- [Official Copilot Documentation](https://docs.github.com/en/copilot)
- [Custom Instructions Guide](https://docs.github.com/en/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot)
- Quality Tools reference in guidelines/
- Commands reference in commands/

---

**Remember:** Effective instructions are concise, specific, and actionable. They guide Copilot to generate code that matches your project's standards and your team's preferences.

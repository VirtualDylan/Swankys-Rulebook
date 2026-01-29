# Cursor IDE AI Rules

## Setup

1. Copy the `.cursorrules` file to the root of your project
2. Cursor will automatically read and apply these rules when you use AI features

### Modern Approach (Recommended)
For Cursor's newer rule system, you can also create individual `.mdc` files in `.cursor/rules/`:

```bash
mkdir -p .cursor/rules
# Create individual rule files as needed
```

Example `.mdc` file with frontmatter:
```markdown
---
description: "Core project coding standards"
globs:
  - "src/**/*.ts"
  - "src/**/*.tsx"
alwaysApply: true
---

# Your rules here
```

## What's Included

### Main Rules File
- **.cursorrules** - Legacy single-file format (still supported)
  - Core development principles
  - Code quality standards
  - Quality & testing requirements
  - Architecture patterns
  - Development workflow guidelines
  - Security & performance best practices
  - Error handling standards
  - Git practices

### Commands
Reusable command templates for structured tasks:
- **5whys.md** - 5 Whys root cause analysis
- **createAgilePlan.md** - Comprehensive feature planning
- **createAgileSprint.md** - Sprint plan generation
- **find-rc.md** - Root cause discovery
- **fishbone.md** - Fishbone diagram analysis
- **outline.md** - Project outline creation
- **rca.md** - Formal root cause analysis reports
- **rcv.md** - Root cause verification
- **solve-rc.md** - Solution implementation

### Guidelines
Reference documentation and detailed methodologies:
- **QualityTools.md** - Six Sigma and Lean tools for software
- **TechnicalSpecifications.md** - Technical spec writing guide
- **MemoryBank.md** - Persistent context documentation
- **Fixing a bug.md** - Bug fixing workflow
- **New Feature.md** - Feature development process
- **New Chat with Directive.md** - Effective prompting guide

## Usage

### Automatic Application
Once `.cursorrules` is in your project root, Cursor automatically:
- Applies rules to AI-generated code
- Follows coding standards in suggestions
- Maintains consistency across the project
- Respects architectural patterns

### Using Commands
Commands provide structured approaches for specific tasks:
1. Reference the command in your Cursor chat
2. Follow the outlined process
3. Cursor will apply the methodology

Example in Cursor chat:
```
Follow the /rca approach to analyze this bug: [describe issue]
```

### Scope-Specific Rules
With `.mdc` files, you can create rules that apply to specific file patterns:
- **Component rules** - Apply only to React components
- **API rules** - Apply only to API routes
- **Test rules** - Apply only to test files

## Best Practices

### Rule Organization
1. **Keep focused** - Rules should be clear and actionable
2. **Be specific** - Vague rules lead to inconsistent results
3. **Use examples** - Show desired patterns when possible
4. **Avoid duplication** - Reference existing files instead of copying
5. **Update regularly** - Keep rules current with your project

### Rule Scoping
- Use `alwaysApply: true` for universal rules
- Use `globs` to target specific file patterns
- Create separate rule files for different concerns
- Avoid overly broad rules that don't fit all contexts

### Integration with Cursor Features
- **Chat** - Rules inform chat responses
- **Autocomplete** - Rules guide inline suggestions
- **Cmd+K** - Rules apply to inline edits
- **Code generation** - Rules shape generated code

## Migrating from .cursorrules to .mdc

If you want to use the modern `.mdc` system:

1. Create `.cursor/rules/` directory
2. Split your `.cursorrules` into focused `.mdc` files
3. Add appropriate frontmatter to each file
4. Keep `.cursorrules` for backward compatibility or remove it

Example migration:
```bash
# Old way
.cursorrules

# New way
.cursor/rules/core-principles.mdc
.cursor/rules/react-patterns.mdc
.cursor/rules/testing-standards.mdc
```

## Customization

Adapt the rules for your project:
- Add language-specific conventions
- Include framework-specific patterns
- Define project-specific standards
- Reference your tech stack documentation
- Add team-specific workflows

## Tips for Effective Rules

### Do's
✅ Be concise and specific
✅ Provide concrete examples
✅ Focus on important patterns
✅ Keep rules under 500 lines per file
✅ Use clear, actionable language
✅ Reference existing code as examples

### Don'ts
❌ Don't write overly long rules
❌ Don't be vague or generic
❌ Don't duplicate existing documentation
❌ Don't make rules too restrictive
❌ Don't forget to update as project evolves

## Troubleshooting

### Rules Not Working
- Ensure `.cursorrules` is in project root
- Check file permissions
- Restart Cursor IDE
- Verify rule syntax

### Inconsistent Application
- Make rules more specific
- Use glob patterns for targeted rules
- Split broad rules into focused ones
- Provide more examples

### Performance Issues
- Keep rule files under 500 lines
- Use multiple small files instead of one large file
- Avoid redundant content
- Reference external docs instead of duplicating

## Integration with Quality Tools

The rules emphasize structured problem-solving:
- Apply quality methodologies from QualityTools.md
- Use root cause analysis for debugging
- Follow PDCA cycle for improvements
- Document learnings and patterns

This creates a consistent, high-quality development experience with Cursor's AI assistance.

# Google Gemini Instructions

## Setup

Google Gemini supports project context through `GEMINI.md` files and uploaded documents.

### For Gemini CLI

1. Copy `GEMINI.md` to your project root:
   ```bash
   cp GEMINI.md /path/to/your/project/
   ```

2. Gemini CLI automatically reads `GEMINI.md` files:
   - Checks current directory
   - Searches parent directories up to project root
   - Loads hierarchically (global → project → directory-specific)
   - Respects `.gitignore` and `.geminiignore`

3. View loaded context:
   ```bash
   gemini /memory
   ```

### Hierarchical Context

You can place `GEMINI.md` files at different levels:

```
~/GEMINI.md                    # User-level defaults
/project/GEMINI.md             # Project-wide instructions
/project/src/api/GEMINI.md     # API-specific instructions
```

Gemini combines all relevant files for context.

### For Gemini Web/Mobile App

1. **Create a Custom Gem:**
   - Click "Create Gem"
   - Add instructions in the text field
   - Copy relevant sections from `GEMINI.md`
   - Save and name your Gem

2. **Use Projects Feature:**
   - Upload relevant files (MD, PDF, code files)
   - Add instructions in project settings
   - Reference uploaded files in conversations

### Modular Context

Within `GEMINI.md`, reference other files:

```markdown
# Main Instructions

Core principles here...

@guidelines/QualityTools.md
@commands/rca.md
```

This keeps the main file focused while importing detailed content.

## What's Included

### Main Instructions File
- **GEMINI.md** - Primary instruction file for Gemini
  - Core development principles
  - Code quality standards
  - Quality assurance methodologies
  - Technical specifications guide
  - Development workflows
  - Testing requirements
  - Security standards
  - Performance considerations
  - Memory Bank pattern
  - Available commands reference

### Commands
Structured templates for common tasks:
- **5whys.md** - 5 Whys root cause analysis
- **createAgilePlan.md** - Feature planning template
- **createAgileSprint.md** - Sprint planning guide
- **find-rc.md** - Root cause discovery process
- **fishbone.md** - Fishbone diagram analysis
- **outline.md** - Project outline creation
- **rca.md** - Root cause analysis reports
- **rcv.md** - Root cause verification
- **solve-rc.md** - Solution implementation

### Guidelines
Reference documentation and methodologies:
- **QualityTools.md** - Quality tools for software engineering
- **TechnicalSpecifications.md** - Technical spec writing guide
- **MemoryBank.md** - Persistent context documentation
- **Fixing a bug.md** - Bug fixing workflow
- **New Feature.md** - Feature development process
- **New Chat with Directive.md** - Effective prompting guide

## Usage

### Automatic Context Loading (CLI)

When using Gemini CLI with `GEMINI.md` in place:

```bash
# Gemini automatically loads context
gemini "How should I structure this new feature?"

# Gemini applies coding standards and methodologies
gemini "Debug this authentication issue"

# Check what context is loaded
gemini /memory
```

### In Gemini App

**Using Custom Gems:**
1. Select your custom Gem for the session
2. Gem applies its instructions automatically
3. Upload additional files as needed

**Using Projects:**
1. Create project with instructions
2. Upload relevant guidelines
3. All chats in project have access to context

### Referencing Commands

In your prompts:

```
Follow the /rca approach to analyze this bug:
[describe the issue]
```

Or reference specific command files:

```
Use the methodology from commands/5whys.md to 
investigate why our API response times increased.
```

### Using Guidelines

Reference guidelines for detailed context:

```
Apply the quality tools from guidelines/QualityTools.md
to improve our testing process.
```

## Best Practices

### Writing GEMINI.md Files

**Do's:**
- ✅ Keep focused and concise
- ✅ Use clear headings and structure
- ✅ Provide concrete examples
- ✅ Reference external files when detailed
- ✅ Update as project evolves
- ✅ Use markdown formatting

**Don'ts:**
- ❌ Don't make files overly long
- ❌ Don't duplicate content across files
- ❌ Don't use vague instructions
- ❌ Don't forget to update with project changes
- ❌ Don't include sensitive information

### Organizing Context

**Single File (Simple Projects):**
```
project/
  GEMINI.md           # All instructions
  src/
  tests/
```

**Multi-File (Complex Projects):**
```
project/
  GEMINI.md                    # Core instructions
  .gemini/
    coding-standards.md
    architecture.md
    workflows.md
  src/
    api/
      GEMINI.md                # API-specific rules
    ui/
      GEMINI.md                # UI-specific rules
```

**Modular Imports:**
```markdown
# GEMINI.md

Core principles...

## Detailed References
@.gemini/coding-standards.md
@.gemini/architecture.md
```

### File Limits and Performance

- Keep individual GEMINI.md files under 2000 words
- Use modular structure for large projects
- Reference external docs instead of copying
- Use `.geminiignore` to exclude unnecessary files

## Supported File Formats

Gemini can process various file types for context:

### Text Files
- `.md` (Markdown) - Primary format
- `.txt` (Plain text)
- `.rtf` (Rich text)

### Documents
- `.pdf` (PDFs)
- `.doc`, `.docx` (Word)
- `.ppt`, `.pptx` (PowerPoint)

### Data Files
- `.csv` (CSV)
- `.json` (JSON)

### Code Files
- `.py`, `.java`, `.cpp`, `.c`, `.php`, `.sql`, `.html`, `.js`, `.ts`, etc.
- Can upload entire code folders (up to 1,000 files on paid plans)

### Images
- `.jpg`, `.jpeg`, `.png`, `.webp`
- Useful for diagrams, architecture visuals

## Advanced Features

### Context Inspection

View loaded context:
```bash
gemini /memory
```

Shows all GEMINI.md files and their sources.

### Temporary Override

Provide temporary instructions in a prompt:
```
For this task only, prioritize performance over readability.
[your request]
```

### Multi-Level Context

Combine general and specific instructions:

```
~/GEMINI.md                   # Personal coding preferences
/project/GEMINI.md            # Project standards
/project/src/api/GEMINI.md    # API-specific patterns
```

Gemini uses all three when working in `/project/src/api/`.

### Ignoring Files

Create `.geminiignore`:
```
node_modules/
dist/
*.log
.env
```

Prevents Gemini from scanning these files.

## Integration with Quality Tools

The instructions emphasize structured problem-solving:

### Root Cause Analysis
- 5 Whys for drilling to root causes
- Fishbone diagrams for complex issues
- Root cause verification before fixing

### Continuous Improvement
- PDCA cycle for implementing changes
- Pareto analysis for prioritization
- Design of Experiments for optimization

### Problem-Solving Workflow
1. Define problem with measurable impact
2. Measure and gather data
3. Analyze using appropriate tools
4. Implement improvements
5. Control and prevent recurrence

See **QualityTools.md** in guidelines for complete methodology.

## Customization

Adapt `GEMINI.md` for your project:

### Language-Specific Rules
```markdown
## Python Standards
- Follow PEP 8
- Use type hints
- Write pytest tests
- Google-style docstrings
```

### Framework-Specific Patterns
```markdown
## React Conventions
- Functional components only
- Hooks for state management
- PropTypes or TypeScript
- Jest + React Testing Library
```

### Project-Specific Context
```markdown
## Our Architecture
- Microservices with REST APIs
- PostgreSQL database
- Redis for caching
- Docker deployment
```

## Troubleshooting

### Context Not Loading

**Check:**
- GEMINI.md is in project directory
- File has correct name (case-sensitive)
- File permissions allow reading
- Not excluded by .geminiignore

**Try:**
- Run `gemini /memory` to see loaded context
- Check for syntax errors in markdown
- Verify file encoding (UTF-8)

### Inconsistent Application

**Solutions:**
- Make instructions more specific
- Provide concrete examples
- Break into focused sections
- Use clear, actionable language

### Performance Issues

**Optimize:**
- Keep files under 2000 words
- Use modular structure
- Reference instead of duplicate
- Clean up outdated instructions

## Examples

### Minimal GEMINI.md
```markdown
# Project Context

React TypeScript application. Use functional components,
strict types, Jest tests. Prioritize readability.

## Code Style
- camelCase for variables
- PascalCase for components
- Explain complex logic
```

### Detailed GEMINI.md
```markdown
# Project Instructions

## Overview
[Project description]

## Tech Stack
- React 18 + TypeScript
- Vite build tool
- TanStack Query
- Tailwind CSS

## Coding Standards
[Detailed standards]

## Testing
[Test requirements]

## Architecture
@.gemini/architecture.md

## Quality Tools
@.gemini/quality-tools.md
```

## Tips for Effective Use

### Do's
✅ Start with core principles
✅ Provide examples of good patterns
✅ Reference command templates
✅ Update instructions regularly
✅ Use modular structure for large projects
✅ Include project-specific context

### Don'ts
❌ Don't make instructions too verbose
❌ Don't duplicate existing documentation
❌ Don't use ambiguous language
❌ Don't forget to version control GEMINI.md
❌ Don't include secrets or credentials

## Resources

- Gemini CLI documentation
- Custom Gems guide
- Commands folder for templates
- Guidelines folder for methodologies
- Memory Bank patterns

---

**Remember:** Effective GEMINI.md files are focused, well-structured, and provide clear guidance. They should evolve with your project and incorporate learnings over time.

# Claude AI Instructions

## Setup

1. Copy the `CLAUDE.md` file to the root of your project
2. Claude will automatically read and apply these instructions when working on your project

### Alternative Locations
- `.claude/CLAUDE.md` - If you prefer separating config files
- `~/.claude/CLAUDE.md` - For user-level defaults (not for version control)

## What's Included

### Main Instructions File
- **CLAUDE.md** - The primary instruction file that Claude reads automatically
  - Project context and core principles
  - Quality tools and methodologies
  - Memory Bank structure
  - Technical specification guidelines
  - Feature development workflows
  - Bug fixing processes
  - Testing and validation requirements

### Commands
Reusable command prompts for common development tasks:
- **5whys.md** - 5 Whys root cause analysis
- **createAgilePlan.md** - Create comprehensive feature plans
- **createAgileSprint.md** - Generate sprint plans
- **find-rc.md** - Find root causes
- **fishbone.md** - Fishbone diagram analysis
- **outline.md** - Create project outlines
- **rca.md** - Formal root cause analysis reports
- **rcv.md** - Root cause verification
- **solve-rc.md** - Solve identified root causes

### Guidelines
Detailed documentation and reference materials:
- **QualityTools.md** - Six Sigma and Lean quality tools for AI coding
- **TechnicalSpecifications.md** - How to write good technical specs
- **MemoryBank.md** - Persistent documentation patterns
- **Fixing a bug.md** - Structured bug fixing workflow
- **New Feature.md** - Feature development template
- **New Chat with Directive.md** - How to start new conversations effectively

## Usage

### Using the Main Instructions
Once you've copied `CLAUDE.md` to your project root, Claude will automatically:
- Read the file at the start of each session
- Apply the coding standards and workflows
- Follow the quality methodologies
- Maintain consistency across interactions

### Using Commands
Commands are reference templates you can use in your prompts:
1. Review the relevant command file
2. Copy or reference the structure in your conversation with Claude
3. Claude will follow the structured approach outlined

Example:
```
I need to do a root cause analysis. Please follow the approach 
outlined in /rca for this issue: [describe your issue]
```

### Using Guidelines
Guidelines provide detailed background and methodology:
- Reference them when you need Claude to understand specific approaches
- Use them as knowledge base for complex workflows
- Adapt them to your specific project needs

## Customization

Feel free to customize `CLAUDE.md` for your project:
- Add project-specific coding standards
- Include your tech stack details
- Add custom commands and workflows
- Reference additional documentation
- Adjust to your team's preferences

## Best Practices

1. **Keep it focused** - CLAUDE.md should be concise and well-structured
2. **Link to other docs** - Use references to keep the main file lean
3. **Version control** - Commit CLAUDE.md to your repository
4. **Use CLAUDE.local.md** - For user-specific overrides (add to .gitignore)
5. **Update regularly** - Keep instructions current with your project evolution

## Integration with Memory Bank

The instructions emphasize using a Memory Bank for persistent context:
- Review the MemoryBank.md guidelines
- Set up the recommended file structure
- Update memory files as your project evolves
- Let Claude read the memory bank at the start of each task

This ensures continuity even when starting fresh conversations.

## Tips

- The quality tools section helps apply structured problem-solving
- Use the technical specification guidelines for clear requirements
- Follow the feature development workflow for new functionality
- Apply the bug fixing process for systematic debugging
- Reference MCP connections when available for enhanced capabilities

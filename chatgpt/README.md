# ChatGPT Custom Instructions

## Setup

ChatGPT allows you to customize how it responds through Custom Instructions (available in user settings) and Projects (for organizing related conversations with shared context).

### Method 1: User-Level Custom Instructions

1. Click your profile icon in ChatGPT
2. Select **Settings** → **Personalization** → **Custom Instructions**
3. Copy the content from `custom-instructions.md`
4. Paste into the two text boxes:
   - **"What would you like ChatGPT to know about you?"** - First section
   - **"How would you like ChatGPT to respond?"** - Second section
5. Save changes

These instructions will apply to all your conversations unless overridden by a Project.

### Method 2: ChatGPT Projects (Recommended)

Projects provide workspace-specific context and instructions:

1. Click **Create new project** in ChatGPT
2. Name your project (e.g., "My App Development", "Bug Fixing Workspace")
3. Add project-specific custom instructions
4. Upload relevant files from the guidelines folder
5. All conversations in this project will have access to instructions and files

### Combining Both Methods

- Use user-level instructions for general preferences
- Use project-level instructions for specific codebases or tasks
- Project instructions override user-level instructions

## What's Included

### Main Instructions File
- **custom-instructions.md** - Custom instructions for ChatGPT
  - What ChatGPT should know about you
  - How ChatGPT should respond
  - Project-specific instruction templates
  - Quality tools reference
  - Memory Bank pattern
  - Commands & templates reference

### Commands
Structured templates for common tasks:
- **5whys.md** - 5 Whys root cause analysis
- **createAgilePlan.md** - Feature planning template
- **createAgileSprint.md** - Sprint planning guide
- **find-rc.md** - Root cause discovery
- **fishbone.md** - Fishbone diagram analysis
- **outline.md** - Project outline creation
- **rca.md** - Root cause analysis reports
- **rcv.md** - Root cause verification
- **solve-rc.md** - Solution implementation

### Guidelines
Reference documentation:
- **QualityTools.md** - Quality methodologies for coding
- **TechnicalSpecifications.md** - Technical spec writing
- **MemoryBank.md** - Persistent documentation patterns
- **Fixing a bug.md** - Bug fixing workflow
- **New Feature.md** - Feature development process
- **New Chat with Directive.md** - Effective prompting

## Usage Patterns

### For General Coding

With custom instructions applied, ChatGPT will:
- Ask clarifying questions before proposing solutions
- Provide structured, step-by-step responses
- Include code examples with explanations
- Consider edge cases and error handling
- Suggest testing approaches
- Follow quality best practices

### For Projects

**Create specialized projects for different needs:**

#### Bug Fixing Project
- **Instructions**: "Use 5 Whys for root cause analysis. Suggest test cases. Recommend simplest effective fix."
- **Files**: Upload QualityTools.md, Fixing a bug.md
- **Use for**: Debugging sessions

#### Feature Development Project
- **Instructions**: "Ask clarifying questions. Break into incremental steps. Consider existing patterns."
- **Files**: Upload MemoryBank.md, New Feature.md, TechnicalSpecifications.md
- **Use for**: Building new features

#### Code Review Project
- **Instructions**: "Check quality, security, tests, docs. Provide constructive feedback."
- **Files**: Upload QualityTools.md, project coding standards
- **Use for**: Reviewing pull requests

#### Architecture Planning Project
- **Instructions**: "Present multiple approaches with trade-offs. Use diagrams. Consider scalability."
- **Files**: Upload systemPatterns.md, techContext.md
- **Use for**: Design decisions

### Using Commands in Chat

Reference commands by name or paste their content:

```
Please follow the /rca approach to analyze this bug:
[Describe the issue]
```

Or paste the entire command template for ChatGPT to follow.

### Uploading Project Files

In a Project, you can upload:
- Your codebase files
- Documentation
- Guidelines from this folder
- Memory Bank files
- Architecture diagrams
- Previous analysis

ChatGPT will reference these files when responding.

## Best Practices

### Writing Effective Instructions

**Keep it concise:**
- 1-2 paragraphs per section
- Focus on most important preferences
- Use bullet points

**Be specific:**
- "Use TypeScript with strict mode" not "use types"
- "Follow PEP 8 style guide" not "write clean Python"
- "Include Jest tests" not "add tests"

**Provide examples:**
- Show preferred code style
- Demonstrate desired response format
- Include sample outputs

### Organizing Projects

**One project per codebase:**
- Keep context focused
- Upload relevant files only
- Update instructions as project evolves

**One project per activity type:**
- Debugging project
- Feature development project
- Learning project
- Architecture project

**Hybrid approach:**
- Main project for primary codebase
- Task-specific projects for special needs

### Maintaining Instructions

1. **Review quarterly** - Update as your preferences evolve
2. **Refine based on results** - Note what works and what doesn't
3. **Remove outdated items** - Keep instructions current
4. **Test changes** - See how adjustments affect responses
5. **Share with team** - Align on standards

## Advanced Features

### Contextual Instructions

For temporary focus within a conversation:

```
For this task, prioritize performance over readability.
```

This applies just to that conversation thread.

### File-Based Context

Upload files that ChatGPT should reference:
- `README.md` - Project overview
- `ARCHITECTURE.md` - System design
- `CONVENTIONS.md` - Coding standards
- Memory Bank files
- Previous analysis documents

### Multi-Turn Workflows

Structure complex tasks across multiple prompts:

1. **Analysis**: "Analyze this bug using 5 Whys"
2. **Options**: "Suggest 3 different solutions"
3. **Selection**: "Let's go with option 2, provide implementation"
4. **Testing**: "What tests should I write?"
5. **Documentation**: "Help me document this fix"

## Tips for Better Results

### Do's
✅ Be specific about what you want
✅ Provide context and examples
✅ Break complex tasks into steps
✅ Use Projects for organized work
✅ Upload relevant documentation
✅ Reference command templates
✅ Iterate on instructions

### Don'ts
❌ Don't make instructions too long
❌ Don't be vague or generic
❌ Don't skip providing context
❌ Don't forget to update instructions
❌ Don't ignore file upload feature
❌ Don't expect mind-reading

## Example Instructions

### Minimal (Good for Beginners)

**What ChatGPT should know:**
"I'm a software developer working on web applications. I prefer simple, readable code and test-driven development."

**How ChatGPT should respond:**
"Be concise. Provide code examples. Explain your reasoning. Suggest tests."

### Detailed (Good for Specific Projects)

**What ChatGPT should know:**
"I'm building a React TypeScript application with strict type checking. I use Jest for testing, follow functional programming patterns, and maintain a Memory Bank for persistent context. I value structured problem-solving using quality tools like 5 Whys and PDCA."

**How ChatGPT should respond:**
"Start with a brief summary. Ask clarifying questions. Present multiple solutions with trade-offs. Use TypeScript with proper types. Include Jest test cases. Follow functional patterns (pure functions, no mutation). Use bullet points and code examples. Reference Memory Bank patterns. Apply quality methodologies for debugging."

## Integration with Quality Tools

The instructions incorporate quality methodologies:

### For Debugging
- Apply 5 Whys to find root cause
- Use Fishbone for complex issues
- Verify causes before fixing
- Document learnings

### For Development
- Follow PDCA cycle
- Plan before implementing
- Test thoroughly
- Refine based on results

### For Improvement
- Use Pareto analysis for prioritization
- Apply FMEA for critical systems
- Document patterns
- Prevent recurrence

See **QualityTools.md** in guidelines for complete reference.

## Troubleshooting

### Instructions Not Applied

**Check:**
- Saved in settings or project
- Not overridden by project (if using user-level)
- Clear and specific wording
- Not contradictory

**Try:**
- Rephrase instructions
- Simplify if too complex
- Test in new conversation
- Use project-level override

### Inconsistent Results

**Solutions:**
- Make instructions more specific
- Provide examples
- Use project context
- Upload reference files
- Break complex instructions into clear points

### Too Verbose or Too Brief

**Adjust:**
- Add "Be concise" or "Be detailed"
- Specify response length
- Use "Use bullet points" or "Provide thorough explanations"
- Give examples of desired format

## Resources

- ChatGPT Projects documentation
- Custom instructions help
- Commands folder for templates
- Guidelines folder for methodologies
- Memory Bank patterns

---

**Remember:** Custom instructions are most effective when they're concise, specific, and aligned with how you actually work. Start simple and refine over time based on the quality of responses you get.

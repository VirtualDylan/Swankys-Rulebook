# Solve Root Cause (/solve-rc)

**Purpose:** Create a solution plan or begin implementing a fix for the issue.

**Prompt:**
1. **Define Issue Name:** Use `$ARGUMENTS[0]` as the unique issue name (e.g., `login-api-500-error`).
2. **Action Mode:** Check `$ARGUMENTS[1]`:
   - `begin` → Start reading relevant files and begin implementing solution.
   - `plan` (or no argument) → Generate a **solution plan** first.
3. **Relevant Files:** Read all analysis and verification files under `./docs/troubleshooting/{issueName}/`.
4. **Generate Solution Plan (if mode = plan or no argument):**
   - Save plan in `./docs/troubleshooting/{issueName}/{issueName}-solution.md`
   - Use the following structure:
            Background
                •	Summary of the issue
                •	Helpful analysis documents (e.g., find-rc, 5whys, fishbone, pareto, rca, verification)
                •	Relevant source code files to use in the solution

            Checklist
                •	High-level development tasks to fix the issue
                •	Include exact components, files, and line numbers
                •	Provide enough detail for a developer to follow

            Testing and Validation
                •	Step-by-step instructions for testing to verify the root cause has been fixed
                •	Include which logs, API responses, or unit/integration tests to check

            Next Steps
                •	Update documentation
                •	Update user guides
                •	Add notes to quality docs if issue is not fully resolved
                •	Any other follow-up tasks after the fix
5. **Begin Implementation (if mode = begin):**
   - Read relevant files and start implementing the solution based on the above plan.
6. **Instructions:**
   - Always reference **full file paths from project root**, components, and line numbers.
   - If generating a plan, ensure it is concise, actionable, and human-readable.
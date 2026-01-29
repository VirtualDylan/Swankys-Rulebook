# Root Cause Identification (/find-rc)

**Purpose:** Identify potential root causes for a bug or issue using structured Six Sigma tools.

**Prompt:**
Perform a structured Root Cause Analysis for the issue described in `$ARGUMENTS`:

1. **Define Issue Name:** Ask for a concise, unique issue name (e.g., `login-api-500-error`) for folder/file naming.
2. **Folder Creation:** Create a folder `./docs/troubleshooting/{issueName}/`.
3. **Problem Summary:** Restate the issue clearly. Include error messages, symptoms, or logs.
4. **Component Identification:** Identify exact components, files, and line numbers involved (full paths from project root).
5. **5 Whys Analysis:** Ask "Why did this happen?" repeatedly to drill down to underlying causes.
6. **Fishbone Analysis:** Create a textual fishbone diagram with categories: People, Process, Code, Environment, Tools, Requirements. List contributing factors.
7. **Pareto Analysis:** Rank causes by likelihood or impact; highlight critical ones.
8. **Documentation:** Save findings in `./docs/troubleshooting/{issueName}/{issueName}-find-rc.md`.
9. **Instructions:** Do **not modify any code**; focus on precise analysis and documentation only.
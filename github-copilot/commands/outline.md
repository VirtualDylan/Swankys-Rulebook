# Documentation Outline (/outline)

**Purpose:** Generate structured outline for troubleshooting or RCA documentation.

**Prompt:**
1. **Define Issue Name:** Ask for unique issue name.
2. **Outline Sections:**
   - Problem Description
   - Evidence / Logs
   - Analysis Steps (tools used: 5 Whys, Fishbone, Pareto)
   - Identified Root Causes
   - Verification Steps
   - Recommended Fix / Prevention
3. **Component References:** Include affected components, files, and line numbers.
4. **Documentation:** Save outline in `./docs/troubleshooting/{issueName}/{issueName}-outline.md`.
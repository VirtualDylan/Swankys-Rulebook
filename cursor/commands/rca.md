# Root Cause Analysis (/rca)

**Purpose:** Produce a formal Root Cause Analysis report using results from `/find-rc`.

**Prompt:**
Using the analysis results:

1. **Define Issue Name:** Ask for the unique issue name.
2. **Summary:** Clearly summarize problem, symptoms, and timeline.
3. **Component References:** Include affected components, full file paths, and line numbers.
4. **Analysis Methods:** Document methods used (5 Whys, Fishbone, Pareto).
5. **Root Causes:** Identify most likely root cause(s).
6. **Recommended Actions:** Include proposed fixes and prevention strategies.
7. **Documentation:** Save report in `./docs/troubleshooting/{issueName}/{issueName}-rca.md`.
8. **Instructions:** Do **not modify code**; this step is for reporting only.
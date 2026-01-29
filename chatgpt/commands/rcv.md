# Root Cause Verification (/rcv)

**Purpose:** Verify hypothesized root causes before applying fixes.

**Prompt:**
For each suspected root cause from `/rca`:

1. **Define Issue Name:** Ask for unique issue name.
2. **Verification Steps:** Suggest tests, log inspections, or simulations to confirm/refute each cause.
3. **Component References:** Include exact files, components, and line numbers.
4. **Results:** Document outcome (Confirmed / Refuted / Inconclusive) for each suspected cause.
5. **Documentation:** Save results in `./docs/troubleshooting/{issueName}/{issueName}-verification.md`.
6. **Instructions:** Do **not fix code automatically**; focus on thorough verification documentation.
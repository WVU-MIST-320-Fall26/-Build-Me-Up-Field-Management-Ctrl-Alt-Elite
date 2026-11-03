# Risk Register: Build Me Up Field Management

**Project:** Field Operations & Change Management Portal
**Project Manager:** Blayne Kuhn
**Last Reviewed:** 2026-11-02 (mid-Sprint 2)

**Scoring:** Probability (1-3) × Impact (1-3) = Risk Score. Critical (7-9), High (5-6), Medium (3-4), Low (1-2).

## Risk Register Table

| ID | Risk Description | Category | Probability (1-3) | Impact (1-3) | Risk Score | Response Strategy | Mitigation Plan | Owner | Status | Last Update |
|---|---|---|---|---|---|---|---|---|---|---|
| R-01 | Offline mode and background sync (#7) produce data conflicts or lost site logs when field users reconnect after working without signal | Technical | 3 (High) | 3 (High) | 9 | Mitigate | Define a conflict-resolution rule (last-write-wins plus a flagged-conflict queue); build automated sync tests for poor and no-signal cases; QA sign-off required before #7 moves to Done | Jack McLaughlin (Systems Architect) | Active | 2026-11-02 |
| R-02 | Accounting system integration (#19) is delayed by unclear API access, data mapping, or vendor turnaround, putting Sprint 3 and the Nov 20 launch at risk | Technical / Schedule | 2 (Medium) | 3 (High) | 6 | Mitigate | Confirm accounting API credentials and field mapping during Sprint 2; build against a mock service first; fall back to a CSV export if the live integration is not ready | Ryan Kirman (Lead BA) | Active | 2026-11-02 |
| R-03 | Stakeholders keep pushing out-of-scope requests (e.g., the smart-wearable / machinery lockout request rejected by the CCB) into the current release | Scope | 2 (Medium) | 3 (High) | 6 | Avoid | Route every new request through the CCB with an impact assessment; log rejected items as deferred Phase 2 backlog issues (#22) with no sprint assigned; PM restates approved scope at each sprint review | Blayne Kuhn (Project Manager) | Active | 2026-11-02 |
| R-04 | Change order approvals do not update budget line items in real time (#11, #12), so PMs see wrong cost figures and the core objective is missed | Technical | 2 (Medium) | 3 (High) | 6 | Mitigate | Write end-to-end test cases from approval to budget update; reconcile dashboard totals against source data during QA; hold #12 in QA until totals match | Jack McLaughlin (QA Lead) | Active | 2026-11-02 |
| R-05 | Field crews resist switching from paper logs to the mobile app, leading to low adoption and incomplete data | Operational | 2 (Medium) | 2 (Medium) | 4 | Mitigate | Run a pilot with one site crew; keep mobile forms short; provide quick-reference guides and on-site training before launch; track weekly submission rates | Blayne Kuhn (Project Manager) | Active | 2026-11-02 |
| R-06 | Small team with one person covering both Systems Architect and QA Lead creates a bottleneck; QA column fills up and WIP limits are exceeded | Resource | 3 (High) | 2 (Medium) | 6 | Mitigate | Enforce Kanban WIP limits (Committed 4, In Progress 3, QA 2); have developers write unit tests before handing off to QA; cross-train the BA to run UAT scripts | Blayne Kuhn (Project Manager) | Active | 2026-11-02 |
| R-07 | Unauthorized access to project, budget, or safety incident data through weak role-based permissions or an exposed cloud setup | Security | 1 (Low) | 3 (High) | 3 | Mitigate | Security review of the role-based access setup (#4) and cloud configuration (#3); least-privilege roles; encryption in transit and at rest; audit trail (#20) logs all changes | Jack McLaughlin (Systems Architect) | Watchlist | 2026-11-02 |
| R-08 | Large blueprint files load slowly or fail on mobile devices in the field, causing crews to fall back on outdated paper drawings | Technical | 2 (Medium) | 2 (Medium) | 4 | Mitigate | Load tests with real drawing sizes before Sprint 3; compress and cache files on the device; show the revision number clearly on every drawing (#9) | Dev Team | Watchlist | 2026-11-02 |

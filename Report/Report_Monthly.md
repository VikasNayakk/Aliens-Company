---
WorkflowId: Report_Monthly
Type: Plural
Category: Reports
Status: Active
Version: 1.0.0
LastUpdated: 2026-07-01
Intent: Generate a professional, audit-ready monthly performance report (24-page futuristic blue-light PDF) for ONE named team member, from the content/data that member provides, using ONE fixed template shared across the whole team and the canonical Aliens design system (shared with Tasks_Report).
Inputs:
  - Targets: REQUIRED single team-member key or name (e.g., "Rajani Rani" or a member id like C1305).
  - Description: REQUIRED monthly content + scope — the member's month summary, metrics, deliverables, challenges, and any explicit include/exclude.
Outputs:
  Path: /Aliens/.Alien/{Developer_Username}/Reports/Report_Monthly/{MemberKey}/{Month_ISO}/{RunId}/
  Artifacts:
    - Intake.md
    - MemberInput.md
    - Scope.Resolve.md
    - Evidence.Inventory.md
    - MonthlyLedger.csv
    - MonthlyLedger.json
    - Content.dict.json
    - MonthlyReport.md
    - MonthlyReport.pdf
    - Report.Quality.md
    - Redaction.Log.md
Calls:
  - Report_Monthly-Planing

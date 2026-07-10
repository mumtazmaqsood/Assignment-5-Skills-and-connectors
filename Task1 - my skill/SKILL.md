---
name: bug-report-format
description: >
  Use this skill whenever the user wants to write, file, draft, or format a
  bug report, issue report, or defect report — whether from scratch, from a
  description of a problem, from logs/screenshots, or from a QA/testing note.
  Triggers on phrases like "bug report", "file a bug", "write up this bug",
  "report this issue", "log a defect", or when the user describes something
  broken and asks for it to be documented. Produces a report with headings in
  this exact fixed order — Environment, then Description (including Logs or
  Screenshots), then Steps to Reproduce, then Expected Result, then Actual
  Result. Always use this skill instead of an ad-hoc format when the
  deliverable is a bug, issue, or defect report.
---
 
# Bug Report Format
 
Produces bug reports with a fixed, consistent structure. Always use the heading
order below — do not reorder, rename, merge, or drop headings, and do not add
extra top-level headings unless the user explicitly asks for more fields.
 
## Heading order (required)
 
1. **Environment**
2. **Description**
   - Sub-section: **Logs / Screenshots**
3. **Steps to Reproduce**
4. **Expected Result**
5. **Actual Result**
## What goes in each section
 
- **Environment** — Where the bug occurs. Include what's known/relevant: OS,
  browser/app version, device, environment (prod/staging/dev), build or
  commit hash, user role/account type. If the user hasn't given these details,
  leave placeholders like `[OS/version]` rather than guessing.
- **Description** — A short (1–3 sentence) plain-language summary of the
  problem: what's wrong and where it happens.
  - **Logs or Screenshots** — Nest this as a sub-heading under Description.
    Paste relevant log excerpts in a code block, or note
    `[Attach screenshot here]` if none were provided. If the user shares logs
    or an image, place them here rather than elsewhere in the report.
- **Steps to Reproduce** — A numbered list, one action per step, starting
  from a clean/known state. Be precise enough that someone unfamiliar with
  the bug could follow along and hit it.
- **Expected Result** — What should happen if the software worked correctly.
- **Actual Result** — What actually happens instead (include error messages,
  codes, or visible symptoms).
## Workflow
 
1. Gather what you can from the conversation (error messages, screenshots,
   steps the user already described, app/environment details).
2. Fill in every section. If information for a section is missing, insert a
   clearly-marked placeholder (e.g. `[not provided]`) rather than inventing
   details — never fabricate log content, versions, or reproduction steps.
3. Output as Markdown using `##` for the five main headings and `###` for
   the Logs/Screenshots sub-heading.
4. If the bug report is a standalone deliverable the user will paste into a
   tracker (Jira, GitHub Issues, Linear, etc.) or share with others, create it
   as a markdown file rather than only printing it inline — see
   `assets/template.md` for the exact skeleton to copy and fill in. For a
   quick one-off in the middle of a conversation, replying inline in the same
   Markdown structure is fine.
## Template
 
See `assets/template.md` for a blank copy of the exact structure to fill in.

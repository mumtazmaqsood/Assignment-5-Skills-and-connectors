# Safety Assessment: Custom Skills Audit

**Skills audited:** `frontend-design` (primary), `bug-report-format` (secondary, for comparison)
**Location:** `/mnt/skills/user/`
**Method:** Full directory listing + full-content review of every file in each skill folder.

---

## 1. frontend-design

**Contents:** One file — `SKILL.md` (~12KB of plain-text instructions). No scripts, binaries, config files, or subfolders.

| Risk area | Finding | Verdict |
|---|---|---|
| External network calls | No URLs, API endpoints, `fetch`/`curl`/`XMLHttpRequest` references, or any instruction to contact a server | ✅ Clear |
| Credential/secret handling | No mention of API keys, tokens, passwords, auth headers, or `.env` files | ✅ Clear |
| Data exfiltration | No instruction to log, transmit, upload, or persist user data outside the conversation | ✅ Clear |
| Executable code | None present — the file is prose guidance only, no scripts run automatically | ✅ Clear |
| Scope of influence | Only shapes *how* I write UI/design code (color, type, layout, copywriting tone) when a design task is triggered | ✅ Narrow, expected scope |
| Prompt injection risk | Content is stable design-studio guidance; no embedded instructions trying to override my behavior, safety policies, or impersonate the user | ✅ Clear |
| Minor packaging issue | Header references `license: Complete terms in LICENSE.txt`, but no `LICENSE.txt` file exists in the folder | ⚠️ Cosmetic only — dangling reference, no functional or security impact |

**Overall:** Low/no risk. This skill is inert text that only steers stylistic and structural choices in generated frontend code. It has no mechanism to reach the network, handle secrets, or move data anywhere.

---

## 2. bug-report-format (comparison reference)

**Contents:** `SKILL.md` + `assets/template.md` (a static blank markdown template). No scripts.

| Risk area | Finding | Verdict |
|---|---|---|
| External network calls | None | ✅ Clear |
| Credential handling | None | ✅ Clear |
| Data exfiltration | None — output is written locally to `/mnt/user-data/outputs/` and only surfaced to you | ✅ Clear |
| Executable code | None | ✅ Clear |

**Overall:** Low/no risk, same profile as above.

---

## General notes on this audit's limits

- This assessment covers *only the two custom skills reviewed*, not Anthropic's built-in skills (docx, pdf, pptx, xlsx, etc.), which do include actual executable scripts and would warrant a separate, more thorough review if you want one — those have more surface area (file I/O, library calls) worth checking.
- "No network calls" reflects what's *written in the skill files*, not a runtime guarantee — skills are instructions I follow, not sandboxed code with enforced permissions. The absence of any network-related instruction is what gives confidence here, rather than a technical block.
- Neither skill contains hidden or obfuscated content (no base64 blobs, no unusual encodings, no non-printable characters) that could hide something not visible in the plain-text review.

**Conclusion:** Both skills are safe as-is — narrowly scoped, plain-text instruction sets with no code execution, no credential handling, and no network or data-transmission behavior.

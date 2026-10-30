---
name: pre-publish-audit
description: The launch-gatekeeper — an adversarial check run on any public marketing draft before the owner sees it for approval - social posts, captions, emails and subject lines, ads, landing pages, product pages, video scripts and on-screen text, press releases, packaging copy. Checks every claim against the claim ledger, catches banned phrases and their paraphrases, hidden "coming soon" dates, implied competitor comparisons, measurement claims disguised as description, fake urgency, missing endorsement disclosures, broken promises, tagline misuse and the comment-section test. Outputs a pass/fail report with exact fixes. Use when someone says "check this before I post", "audit this copy", "is this compliant", "review this email before it goes out", "can we say this", "launch check", "gate this", or whenever another role finishes a public draft.
version: 1.0.0
tags: [marketing, compliance, copy-review, brand-safety, quality-assurance, launch]
---

# Pre-Publish Audit · Launch Gatekeeper

Every public draft passes this gate before it reaches `04_APPROVALS/`. The point is not to polish. The point is to find what will embarrass the owner, break a promise, or create legal exposure, while it's still cheap to fix.

**Run it independently.** The audit must be done by an agent or subagent that did not write the draft. Give it this skill, the draft, `00_BRAIN/COMPANY_BRAIN.md` (sections 5 Voice and 6 Brand laws) and `00_BRAIN/CLAIM_LEDGER.md`, and tell it: *find violations; do not approve.* Self-review checks a draft against what the writer meant. An auditor checks it against what it says, which is why copy its writer believes is clean still fails a fresh read.

Role file: `roles/launch-gatekeeper.md`. Full checklist: `references/audit-checklist.md`.

## Procedure

1. **Load the law.** Read brand laws, voice rules and the whole claim ledger (VALIDATED, PENDING, REFUSED).
2. **Inventory every claim.** List each statement in the draft that asserts something checkable: specs, sizes, speeds, results, compatibility, stock, price, dates, "best/first/only", reviews, comparisons. Include subject lines, image text, video on-screen text, alt text and hashtags.
3. **Run the checklist** in `references/audit-checklist.md`, in order. The first six traps catch most problems.
4. **Classify each finding:**
   - `✗ BLOCK` — can't go out as written (unvalidated claim, refused phrase, legal exposure, broken promise).
   - `⚠ FIX` — should change before approval (voice drift, weak comment-section test, missing alt text).
   - `· NOTE` — owner's call (taste, optional improvement).
5. **Write the exact fix** for every BLOCK and FIX: the replacement wording, or "remove", or "needs claim P# validated: board row #__".
6. **Check internal consistency.** If one claim is blocked, block its twin elsewhere in the draft or campaign.
7. **Verdict:** PASS (no BLOCK, no FIX) · PASS WITH FIXES (fixes applied, re-checked) · BLOCKED (needs the owner or a validation first).
8. **File the report** next to the draft and log any new board rows.

## Report format

```
# Audit · <draft name> · <date>
Auditor: launch-gatekeeper (independent of: <writer role>)
Verdict: PASS / PASS WITH FIXES / BLOCKED

## Claims inventory
| # | Claim as written | Ledger status | Finding |

## Findings
✗ BLOCK 1 — <where: line/subject/frame> — <what's wrong> — Fix: <exact wording or action>
⚠ FIX 1 — …
· NOTE 1 — …

## New board rows
- #__ Validate "<claim>" · owner: <role> · due: <date>

Filed: 04_APPROVALS/YYYY-MM-DD_<role>_<slug>_AUDIT.md
```

## When a claim can't be validated
Don't soften the copy and move on. Raise it as a board row with an owner and a date. One validated claim often unblocks several pieces at once, and soft copy around an unproven claim usually still implies it.

## Pairs with
`marketing-chief-of-staff` (owns the folder, ledger and approvals flow) and every department skill that produces public work.

---
name: uk-job-search-evening-close
description: Audit the scheduled UK job-search close with a concise action ledger, Gmail draft verification, and state updates without taking outbound action.
disable-model-invocation: true
user-invocable: true
---

# UK job-search evening close

## When to use

Use for the scheduled evening close in the jobs project folder, or when asked to audit its daily commitments, Gmail, application state, and clocks. Do not use to discover jobs, draft outreach, or submit/send anything.

## Inputs to gather

1. Read the newest entries in `daily-brief.md` and `job-search-state.json`.
2. Check Sent mail, the dedicated full draft listing, and actionable inbound.
3. Identify deadline and admin clocks and actions in channels that are not visible to the workspace.

## Procedure

1. Classify each current action plainly as `SHIPPED`, `STAGED-NOT-SENT`, `NOT STARTED`, or `INBOUND-UNACTIONED`.
2. Use the dedicated draft-listing tool with full view and a sufficient page size; never infer draft status from `in:draft` search.
3. Verify claimed submissions against direct evidence. An Ashby success page plus form disappearance establishes submission even if there is no email.
4. Keep actions in LinkedIn or WhatsApp `UNCONFIRMED` unless user-supplied evidence establishes completion.
5. After three consecutive closes, replace repetition with the actual blocker or needed decision/person.
6. Append the concise dated close to `daily-brief.md` with one insertion operation. Verify the insertion neighborhood and EOF, then update `job-search-state.json` only for evidenced changes. If application status, pay, or next-step changes, refresh the application board or explicitly report it BLOCKED. Never send messages, submit applications, accept times, create accounts, or solve CAPTCHAs.

## Efficiency plan

- Start with the brief and state file; use one dedicated draft-listing call rather than multiple Gmail searches.
- Reuse already-recorded application proof only as historical context; recheck live clocks before presenting them as current.
- Stop at a readiness report whenever the next operation is user-authorized outbound action.

## Pitfalls and fixes

- Draft search says empty -> it can be a false empty; use dedicated full draft listing.
- An invisible-channel action looks overdue -> do not infer it is incomplete or complete; mark it unconfirmed.
- No confirmation email after an Ashby success page -> do not reapply; record the on-page proof.
- A stale open state appears in the ledger -> seek current evidence or preserve the user-confirmed provenance caveat.
- An append/move leaves duplicate or truncated brief text -> use one atomic insertion and inspect both the target area and file tail before reporting completion.
- A state read fails or a connector times out -> retry and label the result BLOCKED/PARTIAL, never empty.

## Verification checklist

- All four ledger statuses are used accurately and the close is phone-readable.
- Sent, full drafts, and actionable inbound were checked.
- No outbound or account-changing action was taken.
- The close entry was appended and any state edit has evidence/provenance.
- The insertion neighborhood and EOF were checked; the board was refreshed or explicitly marked BLOCKED if status/pay/next-step changed.
- Three-night stalls state a blocker rather than restating the task.

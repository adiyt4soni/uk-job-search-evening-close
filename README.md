# UK job-search evening close (Codex)

Codex version of the nightly check that today's committed actions actually went out: sent mail, real draft list, unanswered inbound.

**Type:** Codex skill · **Area:** Job search automation

## What it does

- Reads today's brief and the tracker, then checks Gmail Sent, the full draft list and actionable inbound.
- Marks each action SHIPPED / STAGED-NOT-SENT / NOT STARTED / INBOUND-UNACTIONED.
- Appends a short dated close to the brief in one atomic insertion and checks the file around it and at the end.

## Guardrails

- Uses the dedicated draft-listing tool, because a draft search can return a false empty.
- Actions in channels it cannot see (LinkedIn, WhatsApp) stay UNCONFIRMED.
- After three nights of the same stall, it names the blocker instead of repeating the item.

## When it triggers

> Audit the scheduled UK job-search close with a concise action ledger, Gmail draft verification, and state updates without taking outbound action.

## What's in this repo

- `SKILL.md`: the skill itself, the file Claude or Codex reads.
- Not included: Nothing beyond the project's own files, which are personal.
- Written to be generic: where the skill relies on the user's own files, it names them by role, not by content.

## Install

```bash
mkdir -p ~/.codex/skills/uk-job-search-evening-close
curl -fsSL https://raw.githubusercontent.com/adiyt4soni/uk-job-search-evening-close/main/SKILL.md -o ~/.codex/skills/uk-job-search-evening-close/SKILL.md
```

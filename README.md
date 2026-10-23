# inspection-sop

**A three-stage quality gate for AI-produced deliverables** — flow check, element
check, and a first-person dry run — packaged as an agent skill (`SKILL.md`).

Most "check this" requests fail because the checker only re-reads the happy path.
This SOP forces three independent passes:

1. **Flow** — completeness, internal/external consistency, accuracy (multi-source),
   usability (renders/opens/runs), process compliance.
2. **Elements** — every fact, number, name, link, date checked against its source;
   time-sensitive values re-fetched; every user requirement traced to where it landed.
3. **Dry run** — walk the deliverable as the real end user would, find the places
   where they would get stuck or run back, simulate failures and edge cases.

Output is a fixed report: scope / method / pass-fail list / fixes / open questions.

## Use it

Copy `SKILL.md` into your agent's skills directory (Claude Code, DeepSeek Harness,
Chatbox, or any agent that loads `SKILL.md` files). The skill triggers on words like
*check / review / verify / QA / re-check / dry-run*.

## Why it exists

Self-produced work is the easiest to over-trust. A structured re-check with a
different reading order catches what a second look does not. The third stage —
pretending to actually use the thing — is where most real defects surface.

## License

MIT — see [LICENSE](LICENSE).

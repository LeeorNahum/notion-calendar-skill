# Maintenance Contract: notion-calendar

This file is for agents editing the skill. Keep maintainer rules here, not in `SKILL.md`.

## Ownership

- `SKILL.md` is the single owner of the calendar rule: the database address, his field names, his title and date conventions, what stays out, and the handoff. It is personal by design, so the database URL and field names belong in it. Other projects point to the skill and keep only what is specific to them.
- `README.md` is the human skim layer. Keep it to a few sentences.

## Sources

- The field and title conventions come from his existing Events rows. When he corrects one, update `SKILL.md`.
- Recheck whether Notion's API and MCP page-update tools persist Date and Location before changing the Working The Page section. If they do, replace the page-UI instruction for those fields.

## Editing Rules

- Keep it short. Add a rule only for a mistake an agent would confidently make without it.
- Examples in `SKILL.md` stay placeholder shapes. Use no real names, events, amounts, or places.
- Do not record dates, row counts, tab titles, or the story of a run.
- Do not add notes, tasks, or reasoning guidance for the calendar itself. The calendar holds events only.
- Do not use em dashes or en dashes, and do not use semicolons to join sentences.
- Quote every frontmatter string value.
- Bump `metadata.version` by the [release-versioning skill](https://app.remoteskill.md/release-versioning-48nJZ5VRGbyq) rules for skills (source: [release-versioning-skill](https://github.com/LeeorNahum/release-versioning-skill)).

## Before Finishing

- Run the skill-forge validator: `npx --yes github:LeeorNahum/skill-forge-skill <skill-root>`.
- `README.md` matches the actual file layout.

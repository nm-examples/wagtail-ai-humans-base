# Base repository development requirements

This repository stores reusable skills and templates, not a runnable Django
application. Use [the development skill](.agents/skills/wagtail-development/SKILL.md)
for planning, changes, and review, applying verification to the affected skills
and templates. Do not attempt application commands at this repository root.
Use `wagtail-bootstrap` when asked to create a separate new site.

Keep changes focused and reviewable, establish expected outcomes before editing,
and explain when a plan should be split. Other skills may supplement this
workflow but must not silently replace it or expand scope. Follow the user's
instructions and applicable instruction hierarchy when resolving conflicts.
Do not weaken verification merely to make an implementation pass; report checks
performed and any gaps.

Maintain both skills and bootstrap resources in sync with the sibling
`wagtail-ai-humans` repository as described in [README.md](README.md). Preserve
independent edits. Keep the development skill's bundled bootstrap copy in sync
with its repository copy. Generated projects receive the bundled project
`AGENTS.md`, not this base-specific file or sibling-mirroring requirements.

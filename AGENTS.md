# Base repository development requirements

This repository stores reusable skills and templates, not a runnable Django
application. Read and follow
[the development skill](.agents/skills/ai-humans-development/SKILL.md)
for planning, changes, and review, applying verification to the affected skills
and templates. Do not attempt application commands at this repository root.
This is required even when another skill provides technical guidance. The
development skill owns the shared scope, verification, Git, and pull-request rules.

For requested code reviews or an agreed review step, also follow
[the code review skill](.agents/skills/ai-humans-code-review/SKILL.md)
for review priorities, evidence, and findings.

Use relevant local technical guidance when maintaining Wagtail templates:

- [Content modeling](.agents/skills/wagtail-content-modeling/SKILL.md): page types,
  snippets, fields, StreamField, editor interfaces, and content migrations.
- [Backend](.agents/skills/wagtail-backend/SKILL.md): queries, search, permissions,
  publishing, workflows, and runtime behavior.
- [Frontend](.agents/skills/wagtail-frontend/SKILL.md): templates, accessibility,
  media rendering, metadata, and editor previews.
- [API](.agents/skills/wagtail-api/SKILL.md): API v3 configuration and integrations.
- [Upgrade](.agents/skills/wagtail-upgrade/SKILL.md): Wagtail upgrade planning and
  implementation.

Read only the technical skills relevant to the task. Apply verification to the
affected resources using configured tools; this repository has no application
to run. Preserve the imported skills'
[provenance and licence material](.agents/skills/PROVENANCE.md) when updating them.

For creating a separate new site, use the
[bootstrap skill](.agents/skills/ai-humans-bootstrap/SKILL.md).
When changing repository skills, follow the copy and mirroring instructions
in [README.md](README.md).

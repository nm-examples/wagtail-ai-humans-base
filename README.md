# Wagtail AI Humans Base

This repository carries eight reusable skills. Three support the project workflow:

- [`ai-humans-bootstrap`](.agents/skills/ai-humans-bootstrap/SKILL.md) creates new
  Wagtail sites using uv, Docker, PostgreSQL, and just, with a fresh dependency
  resolution and lockfile for each site.
- [`ai-humans-development`](.agents/skills/ai-humans-development/SKILL.md) guides
  ongoing application work and owns the shared development, Git, and pull-request
  rules.
- [`ai-humans-code-review`](.agents/skills/ai-humans-code-review/SKILL.md) reviews
  current changes or a requested area for actionable findings, using evidence and
  consistent severity. Invoke it with `$ai-humans-code-review`; it supplements the
  development workflow and loads relevant technical guidance.

Five imported skills supplement that workflow:

| Skill | Use for |
| --- | --- |
| [`wagtail-content-modeling`](.agents/skills/wagtail-content-modeling/SKILL.md) | Page types, snippets, fields, StreamField, editor interfaces, and content migrations. |
| [`wagtail-backend`](.agents/skills/wagtail-backend/SKILL.md) | Queries, search, permissions, publishing, workflows, and runtime behavior. |
| [`wagtail-frontend`](.agents/skills/wagtail-frontend/SKILL.md) | Templates, accessibility, media, metadata, and editor previews. |
| [`wagtail-api`](.agents/skills/wagtail-api/SKILL.md) | API v3 configuration and integrations. |
| [`wagtail-upgrade`](.agents/skills/wagtail-upgrade/SKILL.md) | Wagtail upgrade planning and implementation. |

Use only the technical skills relevant to a task. `ai-humans-development` owns
the shared workflow, and references to linting or frontend builds apply when
those tools are configured. The imported skills' source commit, preserved licence
material, and update process are recorded in
[the provenance notes](.agents/skills/PROVENANCE.md).

[AGENTS.md](AGENTS.md) describes how to maintain these resources in this base
repository, which has no runnable application of its own.

The matching working copy is maintained in the sibling `wagtail-ai-humans`
repository. Updates to all eight skills are mirrored between these repositories,
including instructions, templates, references, UI metadata, and resource additions
or removals. Preserve independent edits in either checkout. When changing
`ai-humans-development`, `ai-humans-code-review`, or an imported technical skill,
also update its bundled directory under
`.agents/skills/ai-humans-bootstrap/assets/templates/.agents/skills/`
and mirror the bootstrap skill as well. Keep provenance and licence material
current in both repositories and their templates. Source-maintenance provenance
notes describe mirroring; the bundled notes are standalone for generated sites.

Invoke the repository-local skill from this checkout and provide a destination
for a separate new project, for example:

```text
$ai-humans-bootstrap Create a site at ../my-new-site named "My New Site".
```

This repository stores the skill; generated applications, lockfiles, database
contents, uploads, and production secrets belong to the destination project.

Each generated site receives its own `AGENTS.md`, `ai-humans-development` and
`ai-humans-code-review` with their UI metadata, and the five technical skills,
including their provenance and licence material, from the bootstrap templates.
These seven skills work without either source repository or a user-level skill
installation and can evolve with the new codebase. Source-specific mirroring
instructions and the bootstrap skill itself are not copied into generated sites.

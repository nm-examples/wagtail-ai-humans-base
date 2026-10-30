# Wagtail AI Humans Base

This repository carries two reusable skills:

- [`wagtail-bootstrap`](.agents/skills/wagtail-bootstrap/SKILL.md) creates new
  Wagtail sites using uv, Docker, PostgreSQL, and just, with a fresh dependency
  resolution and lockfile for each site.
- [`wagtail-development`](.agents/skills/wagtail-development/SKILL.md) guides
  ongoing application work and owns the shared development, Git, and pull-request
  rules.

[AGENTS.md](AGENTS.md) describes how to maintain these resources in this base
repository, which has no runnable application of its own.

The matching working copy is maintained in the sibling `wagtail-ai-humans`
repository. Updates to both skills are mirrored between these repositories,
including instructions, templates, references, UI metadata, and resource additions
or removals. Preserve independent edits in either checkout. When changing the
development skill, also update its bundled copy under
`.agents/skills/wagtail-bootstrap/assets/templates/.agents/skills/wagtail-development/`
and mirror the bootstrap skill as well.

Invoke the repository-local skill from this checkout and provide a destination
for a separate new project, for example:

```text
$wagtail-bootstrap Create a site at ../my-new-site named "My New Site".
```

This repository stores the skill; generated applications, lockfiles, database
contents, uploads, and production secrets belong to the destination project.

Each generated site receives its own `AGENTS.md` and
`.agents/skills/wagtail-development/`, including UI metadata, from the bootstrap
templates. These work without either source repository or a user-level skill
installation and can evolve with the new codebase. Source-specific mirroring
instructions and the bootstrap skill itself are not copied into generated sites.

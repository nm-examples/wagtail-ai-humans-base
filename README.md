# Wagtail AI Humans Base

This repository captures the reusable
[`wagtail-bootstrap` skill](.agents/skills/wagtail-bootstrap/SKILL.md) and its
templates. It creates new Wagtail sites using uv, Docker, PostgreSQL, and just,
with a fresh dependency resolution and lockfile for each site.

The matching working copy is maintained in the sibling `wagtail-ai-humans`
repository. Skill updates are copied here, including instructions, templates,
references, UI metadata, and resource additions or removals.

Invoke the repository-local skill from this checkout and provide a destination
for a separate new project, for example:

```text
$wagtail-bootstrap Create a site at ../my-new-site named "My New Site".
```

This repository stores the skill; generated applications, lockfiles, database
contents, uploads, and production secrets belong to the destination project.

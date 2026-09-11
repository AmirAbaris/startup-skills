# startup-skills

My go-to coding-agent workflow, assembled from other people's skills rather than written from scratch. Open source so it's easy to drop into any project and easy to fork.

The workflow itself — the pipeline order and what each stage does — lives in [AGENTS.md](./AGENTS.md). That's the file to copy into a project so agents there know when to reach for each skill; it assumes the skills are already installed.

## What's in here

Nothing reimplemented. This repo sequences three external skill sources into one pipeline:

- [mattpocock/skills](https://github.com/mattpocock/skills) — `grill-with-docs`, `grilling`, `domain-modeling`, `to-spec`, `to-tickets`, `implement`, `code-review` — the idea → ship spine.
- [cursor/plugins](https://github.com/cursor/plugins) (`unslop`) — strips AI-slop phrasing from generated prose.
- [AmirAbaris/mapping-external-data-to-domain-models](https://github.com/AmirAbaris/mapping-external-data-to-domain-models) — the DTO → domain mapping pattern this workflow applies during implementation.

## Use it in a project

```bash
npx skills@latest add mattpocock/skills --skill grill-with-docs grilling domain-modeling to-spec to-tickets implement code-review
npx skills add https://github.com/cursor/plugins --skill unslop
npx skills add AmirAbaris/mapping-external-data-to-domain-models

cp AGENTS.md /path/to/project/AGENTS.md
```

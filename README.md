# startup-skills

My go-to coding-agent workflow, assembled from other people's skills rather than written from scratch. Open source so it's easy to drop into any project and easy to fork.

The workflow itself — the pipeline order, what each stage does, and the exact install commands — lives in [AGENTS.md](./AGENTS.md). That's the file to copy into a project.

## What's in here

Nothing reimplemented. This repo sequences three external skill sources into one pipeline:

- [mattpocock/skills](https://github.com/mattpocock/skills) — `grill-with-docs`, `grilling`, `domain-modeling`, `to-spec`, `to-tickets`, `implement`, `code-review` — the idea → ship spine.
- [cursor/plugins](https://github.com/cursor/plugins) (`unslop`) — strips AI-slop phrasing from generated prose.
- [AmirAbaris/mapping-external-data-to-domain-models](https://github.com/AmirAbaris/mapping-external-data-to-domain-models) — the DTO → domain mapping pattern this workflow applies during implementation.

## Use it in a project

```bash
cp AGENTS.md /path/to/project/AGENTS.md
cd /path/to/project
# then run the install commands at the top of AGENTS.md
```

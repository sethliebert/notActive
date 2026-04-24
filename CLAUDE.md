# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A personal "master" workspace that will hold multiple independent projects side by side — a mix of personal experiments and work projects — under one git history. The tree is currently empty except for this file; treat it as a fresh start.

## Layout convention

One project per top-level directory, named after the project:

```
./work-acme-dashboard/
./scratch-graph-ideas/
./some-personal-project/
```

- Nothing substantive lives at the repo root. Root holds only this `CLAUDE.md`, a top-level `README.md` if added, and shared config the user explicitly places here.
- Each project owns its own toolchain — its own `pyproject.toml` / `package.json` / lockfile. No shared dependency files across projects.
- Each project has its own `README.md` covering what it is and how to run it. Larger or non-obvious projects can also add a project-level `CLAUDE.md`; Claude Code reads nested `CLAUDE.md` files in addition to this one, and the nested file wins on conflicts.
- A commit or branch should touch one project unless the change is genuinely cross-cutting (this file, shared tooling).

## Projects index

_Add one bullet per project as it lands; keep details in the project's own README._

_(no projects yet)_

## Working here

- Figure out which project the request is about before acting. If more than one project exists and it's ambiguous, ask.
- `cd` into the project directory before running its build/test/lint commands — don't assume root-level tooling exists.
- If a project has its own `CLAUDE.md`, read it before making non-trivial changes in that directory.

## Branches and commits

- Default branch: `master`.
- Branch names scoped to a project: `work-foo/fix-login`, `scratch-graph-ideas/try-force-layout`. Claude-initiated branches may use the `claude/<topic>-<id>` form.
- Commit subjects prefixed with the project directory when project-specific: `work-foo: fix login redirect`.

## Keeping this file short

When a project is added, update the **Projects index** above with one line and push the rest into that project's own `README.md` or `CLAUDE.md`. Resist growing this file — it's meant to be a scannable map, not documentation.

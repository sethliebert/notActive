# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository status

This repository is currently empty. The working tree contains no source files, build config, tests, or tooling — only the `.git` directory and this file.

The git history shows it once hosted a small Python project called `leagueApp` (a League of Legends helper with `main.py`, `champion.py`, `user.py`, and a `championList.txt` data file), but every one of those files was removed in the six most recent commits on `master` (see `git log --oneline`). No replacement code has been added.

## Implications for working here

- There is nothing to build, lint, run, or test. Do not invent commands or infer a toolchain — none is configured.
- There is no architecture to describe yet. Any "big picture" would be fabricated.
- If the user asks you to make changes, first clarify what they want to build, since this is effectively a fresh project. If they want to restore the old code, it can be recovered from history (e.g. `git show 9ec711c:main.py`).
- Active development is happening on branch `claude/add-claude-documentation-Q2wql` (the branch this file was added on); `master` holds the deletion commits.

Update this file as soon as real code, dependencies, or workflows land — the guidance above is only accurate while the tree is empty.

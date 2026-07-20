# Git Workflow

This document defines the Git workflow used throughout the NerfexOS project.

---

# Branch Strategy

During early development, all work is committed directly to the `main` branch.

Feature branches may be introduced after the project reaches beta.

---

# Commit Style

NerfexOS follows the Conventional Commits specification.

Format:

<type>: <short description>

Examples:

feat: add project structure

docs: add roadmap

refactor: reorganize boot scripts

fix: correct plymouth configuration

style: update README formatting

perf: optimize boot services

build: update install script

chore: clean unused files

---

# Commit Rules

- One logical change per commit.
- Do not mix unrelated changes.
- Keep commit messages under 72 characters.
- Use present tense.
- Do not end commit messages with a period.

Good:

feat: add package manifests

Bad:

updated many files

---

# Version Tags

Every release receives an annotated Git tag.

Example:

git tag -a v0.0.1 -m "Initial project structure"

---

# Release Process

1. Complete the planned milestone.
2. Update CHANGELOG.md.
3. Update README if required.
4. Commit changes.
5. Create Git tag.
6. Push commit and tag.

---

# Repository Philosophy

The Git history should clearly describe how NerfexOS evolved over time.

Every commit should answer one question:

"What changed?"
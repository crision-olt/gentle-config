# Code Review Rules

This repository holds agent and editor configuration: markdown skills, JSON config, and shell snippets.

## Commits
- Commit messages follow Conventional Commits v1.0.0 (see `.copilot/skills/conventional-commits/SKILL.md`).
- No `Co-Authored-By` or AI attribution trailers.

## Secrets
- No tokens, API keys, passwords, or credentials in any file.
- Flag absolute paths containing private data or personal identifiers.

## Skills (`SKILL.md`)
- Must start with valid frontmatter: `name`, `description`.
- `description` must include a `Trigger:` clause.
- Keep instructions concrete and free of contradictions with other skills.

## JSON / Config
- Must be valid JSON; no trailing commas or comments.

## Shell
- Quote variables; no destructive commands without guards.

## General
- Keep changes focused; flag unrelated edits in the same commit.

# cursorSkill

Cursor project rules (`.mdc`) that guide AI behavior in this workspace.

## Rules

| Rule | Purpose |
|------|---------|
| [`auto-commit-push.mdc`](.cursor/rules/auto-commit-push.mdc) | Commit and push after completed user-requested changes (conventional commits, safety guards). |
| [`no-write-folder.mdc`](.cursor/rules/no-write-folder.mdc) | Keep `path/to/folder/**` read-only for the AI (reads allowed; writes blocked). |
| [`token-budget.mdc`](.cursor/rules/token-budget.mdc) | Reduce token use: minimal reads, narrow search, small edits, brief replies. |

All rules use `alwaysApply: true` so they apply in every session.

## Setup

1. Clone or copy this repo into your project (or merge `.cursor/rules/` into an existing repo).
2. Edit paths and behavior in each `.mdc` file as needed (e.g. replace `path/to/folder` in `no-write-folder.mdc`).
3. Open the project in Cursor — rules load automatically from `.cursor/rules/`.

## Customize

- **Protected folder:** Update every `path/to/folder` reference in `no-write-folder.mdc`.
- **Git automation:** Adjust commit prefixes or exclusions in `auto-commit-push.mdc`.
- **Token limits:** Tune sections in `token-budget.mdc` for your team’s style.

## Layout

```
.cursor/rules/
  auto-commit-push.mdc
  no-write-folder.mdc
  token-budget.mdc
```

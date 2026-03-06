# Commit Convention

effectorHQ uses a lightweight commit convention based on [Conventional Commits](https://www.conventionalcommits.org/). The goal is readable history, not bureaucracy.

## Format

```
<type>: <description>

[optional body]

[optional footer]
```

### Type

| Type | When to use |
|------|-------------|
| `feat` | A new feature or capability |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `test` | Adding or updating tests |
| `chore` | Build process, CI, dependencies, tooling |
| `style` | Formatting, whitespace (no logic change) |
| `perf` | Performance improvement |

### Description

- Use imperative mood: "add connector" not "added connector"
- Lowercase, no period at the end
- Keep it under 72 characters
- Be specific: "fix auth timeout on retry" not "fix bug"

### Scope (optional)

You can add a scope in parentheses to indicate the area of change:

```
feat(connector): add Slack integration
fix(auth): resolve token refresh race condition
docs(readme): update installation steps
```

## Examples

```
feat: add PostgreSQL connector

Implements a connector for PostgreSQL databases using asyncpg.
Supports read, write, and schema introspection operations.

Closes #42
```

```
fix: prevent duplicate webhook registrations

The registration endpoint was not checking for existing hooks
before creating new ones. Added a uniqueness check on the
callback URL.
```

```
docs: add plugin development quickstart
```

```
chore: upgrade pytest to 8.x
```

## Breaking changes

If your commit introduces a breaking change, add `BREAKING CHANGE:` in the footer:

```
feat: change plugin config format to TOML

BREAKING CHANGE: Plugin configuration files must now use TOML
format instead of JSON. See migration guide in docs/migration.md.
```

## What NOT to do

- `update stuff` — too vague
- `WIP` — use Draft PRs instead of WIP commits
- `fix fix fix` — squash before merging
- Mixing unrelated changes in one commit — keep commits atomic

## Tools

If you use VS Code, the [Conventional Commits](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits) extension can help. Most editors have similar plugins.

For automated enforcement, repos may include [commitlint](https://commitlint.js.org/) configuration.

---

This convention is a guideline, not a gate. If you're unsure, just write a clear message. We can always adjust during review.

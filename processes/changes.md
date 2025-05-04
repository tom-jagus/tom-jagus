# 🔧 Making Changes

This document outlines the process for making structured changes to a project. It applies to all types of work, including feature development, bug fixes, refactoring, documentation, and testing.

The goal is to ensure that each change is:

- Scoped and focused
- Easy to review
- Traceable through clear commits
- Validated before merging

## 🔄 Types of Changes

All changes fall into one of the following categories. Each type has its own naming convention, expectations, and commit style.

### `feat/` — Feature

Used for introducing new functionality or capabilities.

- Examples: adding a new plugin, introducing an automation script, implementing a CLI flag
- Often includes multiple commits: scaffolding → refinement → validation
- Should be tested before merging

---

### `fix/` — Bug Fix

Used for resolving defects, errors, or regressions.

- Examples: correcting a broken alias, resolving an invalid selector in scraping logic
- Focused and minimal — avoid bundling with other unrelated changes
- Include a test or confirmation step when possible

---

### `refactor/` — Refactoring

Used for improving code structure without changing functionality.

- Examples: splitting large files, improving readability, reducing repetition
- Avoid combining with features or fixes
- Recommended to commit separately from behavior changes

---

### `docs/` — Documentation

Used for updating markdown files, in-line comments, or usage instructions.

- Examples: editing `README.md`, adding docstrings, writing standards docs
- Can be merged independently from code

---

### `test/` — Testing and Validation

Used for adding or adjusting test cases, linter configs, or runtime checks.

- Examples: adding RUFF configs, testing a new script, adjusting validation logic
- Should not introduce behavior changes — isolate from `feat/` or `fix/` work

## 🧱 Structuring Commits

Commits should be written as atomic, focused units of change. Each commit should clearly describe what it does, why it matters, and how it fits within the broader goal of the branch.

### Guidelines

- **One idea per commit** — avoid bundling unrelated changes together
- **Use present-tense, imperative style**
  - ✅ `Add Git alias wrapper`
  - ❌ `Added new Git alias wrapper`
- **Keep commits small but meaningful** — not every keystroke, but not a huge dump either
- **Separate logic and documentation** — commit docs, formatting, and features separately

### Recommended structure

When possible, use the following style:

```bash
<type>: <short summary>

# Examples:
feat: Add startup script for Neovim config
fix: Correct Git alias command for PR cleanup
docs: Document branching workflow and process
```

Use a consistent prefix when appropriate, but avoid redundancy if the branch and PR already provide that context.

## ✅ Testing & Validation

All changes should be tested or validated before merging. The level of testing depends on the change type, but the goal is the same: confirm the work does what it’s supposed to, and doesn’t break anything else.

### Manual validation

- Confirm expected behavior through real use or test cases
- Check output, logs, or generated files when applicable
- Re-run scripts or config reloads to ensure changes take effect

### Linting and format checks

- Use static analysis tools (e.g., `ruff`, `shellcheck`, `luacheck`) when applicable
- Resolve warnings or format issues before opening a PR

### What to check per change type

| Change Type | Validation Approach                                     |
| ----------- | ------------------------------------------------------- |
| `feat/`     | Run the new feature and confirm expected behavior       |
| `fix/`      | Reproduce the bug before and confirm it’s resolved      |
| `refactor/` | Compare results before and after — no functional change |
| `docs/`     | Proofread, check formatting, test any code blocks       |
| `test/`     | Confirm that added tests execute and pass               |

If automated tests or checks exist, they should pass before merging. When working solo, manual confirmation is sufficient if it’s documented in the PR or commit.

## 📌 Scope Discipline

Changes should remain focused on a single purpose. Mixing multiple types of work into a single branch or commit increases the risk of errors and makes reviews more difficult.

### Guidelines

- Keep each branch focused on a single task or problem
- Avoid combining:
  - Features with refactors
  - Fixes with unrelated documentation
  - Formatting with logic changes
- Break large changes into logical commits, even if they land in one PR
- If the scope grows unexpectedly, consider splitting the work into a separate branch or future task

### Examples

| ✅ Good practice                    | 🚫 To avoid                        |
| ----------------------------------- | ---------------------------------- |
| `feat: Add logging wrapper`         | `feat: Add logging + refactor CLI` |
| `fix: Handle null values in report` | `fix: Update formatting + fix bug` |
| `docs: Document naming standards`   | `feat: Add alias + docs + tests`   |

Clear scope makes it easier to review, test, revert, or reuse work later.

## 🔁 Final Review Checklist

Before opening a pull request, confirm the following:

- [ ] The change is focused and stays within its intended scope
- [ ] All changes have been tested or validated
- [ ] Each commit is purposeful and clearly written
- [ ] No unrelated formatting, cleanup, or leftover debug code is included
- [ ] The branch name and PR title accurately describe the change

Optional (but recommended):

- [ ] The PR description explains the reasoning behind the change
- [ ] Any known side effects or limitations are noted
- [ ] Related standards or documentation were updated (if relevant)

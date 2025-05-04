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

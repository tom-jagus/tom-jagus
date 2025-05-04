# 🌿 Branching

This document outlines the branching strategy used across all repositories. It is based on a lightweight implementation of GitHub Flow and is designed to support clean version control, isolated development, and consistent merging practices.

All work is performed in branches and merged into the `main` branch through pull requests.

## 📌 Overview

The following rules apply to all repositories that use this branching model:

- The `main` branch always reflects a deployable or ready-to-use state
- All development work is done in separate branches
- Branches are named based on the type and scope of the change
- All changes are merged into `main` via a pull request
- Pull requests serve as checkpoints for review, testing, and documentation
- Branches are deleted after successful merge

## 🧱 Branch Naming Conventions

Branches use consistent prefixes to indicate the type of work being done. This improves readability, helps with automation, and allows for easier filtering in Git and GitHub interfaces.

Use the following format:

```bash
[prefix]/short-description
```

Keep descriptions concise, lowercase, and hyphen-separated.

| Prefix    | Purpose                            | Example                 |
| --------- | ---------------------------------- | ----------------------- |
| feat/     | New features or capabilities       | feat/git-aliases        |
| fix/      | Bug fixes or technical corrections | fix/wrong-alias         |
| refactor/ | Non-functional code improvements   | refactor/config-cleanup |
| docs/     | Documentation updates or additions | docs/branching-process  |
| test/     | Testing or quality-related changes | test/ruff-integration   |

Additional prefixes may be used when necessary, but these are the default set across all repositories.

## ⚙️ Creating a Branch

Branches should be created for every change, regardless of scope. This includes features, fixes, refactoring, testing, and documentation updates.

### 🧭 Manual method

Use the following command to create a new branch:

```bash
git checkout -b feat/short-description
```

Replace the prefix based on the change type. Use lowercase and hyphens in the description.

### ⚡ Using Git alias wrapper

For consistency and speed, a custom hf (Hub Flow) alias system is available:

```bash
git hf feat short-description
```

This command:

- Creates the branch with the correct naming pattern
- Checks it out immediately
- Optionally pushes it to remote (configurable in alias script)

The alias system is defined in the Git configuration file.

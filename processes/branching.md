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

## 🔁 Pull Request Workflow

All changes are merged into `main` through a pull request (PR). This process applies to all repositories, regardless of team size or project scope.

### Key practices

- Every branch is merged via a pull request — never directly to `main`
- Pull requests are used to:
  - Review code before merging (even when working solo)
  - Validate that all intended changes are correct and complete
  - Add meaningful context to the change via the PR description
  - Trigger automated tests, linters, or GitHub Actions when applicable

### PR titles and descriptions

- The title should match the branch name (or summarize it clearly)
- The description should include:
  - A brief explanation of what was done and why
  - Any notes for future reference
  - Links to related issues, if applicable

### Merging and cleanup

After a successful review and test pass:

- The branch is merged using “Squash and merge” or “Rebase and merge” (based on repo settings)
- The local and remote branch is deleted using:

```bash
git hf done
```

This command switches back to `main`, pulls updates, and deletes the merged branch locally and remotely.

## 🧹 Branch Maintenance

Branch hygiene is important for keeping repositories clean, understandable, and easy to navigate.

- Branches should be:

  - Short-lived
  - Task-focused
  - Scoped to a single change or goal

- Avoid:

  - Combining unrelated changes into one branch
  - Leaving branches open after a merge
  - Using generic branch names (e.g., `update`, `fixes`, `test-1`)

- After merging:
  - Always delete the branch (locally and remotely)
  - Ensure `main` is up to date before starting new work
  - Optionally tag the repository if the change warrants a version bump (see: `releases.md`)

Regular branch maintenance prevents merge conflicts, simplifies history, and keeps automation workflows reliable.

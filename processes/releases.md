# 🚀 Releases

This document defines how releases are managed across repositories. It provides a consistent approach to versioning, tagging, and publishing meaningful changes — whether the repository contains config files, automation scripts, personal tools, or documented standards.

Releases help ensure that important milestones are:

- Easy to trace and reproduce
- Properly versioned
- Documented for future reference

## 📦 What Counts as a Release

A release marks a meaningful, traceable point in the evolution of a repository. Not every merged change needs a release — only those that represent a completed unit of progress or introduce notable change.

Releases are typically created when:

- A new feature is added or major capability is completed
- A large configuration or structure change is introduced
- Breaking changes are made that affect usability or compatibility
- A tool, config, or workflow is considered stable enough to reuse
- A milestone is reached (e.g., MVP ready, full migration complete)

Routine updates (e.g., typos, minor formatting, non-functional tweaks) do not require tagging unless they’re part of a larger bundled change.

## 🏷️ Versioning Strategy

All releases follow a simple semantic versioning format:

```
<major>.<minor>.<patch>
```

Example: `0.3.1`

This format is used to communicate the scope of change and expected impact.

### Version bump rules

- `MAJOR` (`1.0.0` → `2.0.0`)  
  Reserved for major redesigns, full rewrites, or backward-incompatible changes.

- `MINOR` (`0.4.0` → `0.5.0`)  
  Used for feature additions, plugin group expansions, or completed functional milestones.

- `PATCH` (`0.4.2` → `0.4.3`)  
  Used for small fixes, polish, or non-breaking improvements.

### Versioning scope

The same versioning format is applied across:

| Repo Type           | Notes                                                                          |
| ------------------- | ------------------------------------------------------------------------------ |
| Config repos        | Bump when structure changes, tools are added, or setup flow is improved        |
| Script/tool repos   | Bump when functionality changes, flags are added, or compatibility is extended |
| Documentation repos | Optional — tag only at major rewrites or clean base snapshots                  |

## 🛠 Creating a Release

Releases are created when a meaningful change has been merged into the `main` branch and is ready to be published, versioned, or reused.

### Release checklist

1. Ensure `main` is up to date:

```bash
  git checkout main
  git pull origin main
```

2. Verify the work meets release criteria (see: What Counts as a Release)

3. Assign the next version number based on the versioning strategy

4. Tag the release:

```bash
git tag -a v0.5.0 -m "Add markdown-focused Neovim plugin group"
git push origin v0.5.0
```

5. (Optional) Create a GitHub release:

- Go to the Releases tab on GitHub
- Select the newly pushed tag
- Write a short release summary (see next section)

### Notes

Tags must use the v prefix (e.g., v0.3.1)

Tags are lightweight and can be created retroactively for past milestones

GitHub releases are optional but recommended for public-facing projects
